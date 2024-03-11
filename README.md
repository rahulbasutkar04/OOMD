# ELECTION RESULT DESIGN

## Classes:
1. `DataExtractor`: public
2. `Enum (PartyName)`: public
3. `VoteCalculator`: private
4. `VoteMapper`: private
5. `DisplayManager`: public

## States:
- `dataFile`: File (private)
- `mappedData`: Map (private)
- `extractedData`: List of map (private)
- `cityNames`: List< of string (private)
- `partyName`: String (private)

## Behavior:
1. `getExtractedData()`: private -> returns List of Map.
2. `getCityNames()`: private -> returns List of String.
3. `getFullNameOfParty()`: private -> returns String.
4. `getMappedData()`: private -> void.
5. `voteComparator()`: private -> returns Map with party code and votes that have the highest count.
6. `cityMapper()`: private -> void.
7. `getResult(mappedData: Map<String, Long>)`: public -> returns void.
8. `displayWinner()`: void

















