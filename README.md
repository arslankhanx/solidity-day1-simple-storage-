# solidity-day1-simple-storage-

pragma solidity 0.6.0;

contract first{
    uint256 public favouriteNumber;
    bool favouritebool;


    struct people {
        uint256 favouriteNumber ;
        string name;
    }
    people[] public People;
    mapping(string => uint256 ) public search;


    //people public person= people ({favouriteNumber:2,name:"Arslan khan"});//
    
    function store(uint256 _favouriteNumber) public {
     favouriteNumber=_favouriteNumber;

    }
    function retrieve() public view returns(uint256){

        return favouriteNumber;
        

    }
    function add(string memory _name, uint256 _favouriteNumber) public  {
        People.push(people({favouriteNumber: _favouriteNumber, name: _name}));
        search[_name]=_favouriteNumber;

    }
}
