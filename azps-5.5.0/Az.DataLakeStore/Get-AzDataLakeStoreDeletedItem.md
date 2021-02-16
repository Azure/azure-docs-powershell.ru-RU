---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: cfcdf8accb5de467c5b243df2c973074fe9ae31a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238203"
---
# <span data-ttu-id="ffa90-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ffa90-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="ffa90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffa90-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa90-103">Поиск удаленных записей в корзине, которые соответствуют фильтру.</span><span class="sxs-lookup"><span data-stu-id="ffa90-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="ffa90-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ffa90-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa90-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffa90-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa90-106">Командлет **Get-AzDataLakeStoreDeletedItem** выполняет поиск удаленных файлов или папок в магазине Data Lake Store в соответствие с заданным фильтром.</span><span class="sxs-lookup"><span data-stu-id="ffa90-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="ffa90-107">Здесь отображаются следующие атрибуты удаленных элементов: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="ffa90-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="ffa90-108">Операция может быть длительной, так как может потребоваться поиск миллионов файлов в корзине и ее можно запустить как задание.</span><span class="sxs-lookup"><span data-stu-id="ffa90-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>
<span data-ttu-id="ffa90-109">Внимание! Неудачание файлов — это лучший способ работы.</span><span class="sxs-lookup"><span data-stu-id="ffa90-109">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="ffa90-110">После удаления файла его можно восстановить без каких-либо гарантий.</span><span class="sxs-lookup"><span data-stu-id="ffa90-110">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="ffa90-111">Использование этого API включено с помощью списка в списках.</span><span class="sxs-lookup"><span data-stu-id="ffa90-111">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="ffa90-112">Если ваша учетная запись ADL не находится в списке, использование этого api позволит не реализовать исключение.</span><span class="sxs-lookup"><span data-stu-id="ffa90-112">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="ffa90-113">Для получения дополнительных сведений и помощи обратитесь в службу поддержки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ffa90-113">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="ffa90-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ffa90-114">EXAMPLES</span></span>

### <span data-ttu-id="ffa90-115">Пример: подробные сведения о файле из магазина Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="ffa90-115">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="ffa90-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffa90-116">PARAMETERS</span></span>

### <span data-ttu-id="ffa90-117">-Account</span><span class="sxs-lookup"><span data-stu-id="ffa90-117">-Account</span></span>
<span data-ttu-id="ffa90-118">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ffa90-118">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa90-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ffa90-119">-AsJob</span></span>
<span data-ttu-id="ffa90-120">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ffa90-120">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa90-121">-Count</span><span class="sxs-lookup"><span data-stu-id="ffa90-121">-Count</span></span>
<span data-ttu-id="ffa90-122">Количество результатов, которые пользователь хочет найти.</span><span class="sxs-lookup"><span data-stu-id="ffa90-122">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="ffa90-123">Запрос выполняется до тех пор, пока не найдет результаты count или не будет ничего делать в корзине ( в зависимости от того, что произойдет раньше).</span><span class="sxs-lookup"><span data-stu-id="ffa90-123">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa90-124">-DefaultProfile</span></span>
<span data-ttu-id="ffa90-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffa90-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffa90-126">-Filter</span><span class="sxs-lookup"><span data-stu-id="ffa90-126">-Filter</span></span>
<span data-ttu-id="ffa90-127">Определяет поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="ffa90-127">Specifies the search query.</span></span> <span data-ttu-id="ffa90-128">Более конкретное значение обеспечивает более релевантные результаты.</span><span class="sxs-lookup"><span data-stu-id="ffa90-128">A more specific value gives more relevant results.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa90-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa90-129">CommonParameters</span></span>
<span data-ttu-id="ffa90-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffa90-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa90-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffa90-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa90-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffa90-132">INPUTS</span></span>

### <span data-ttu-id="ffa90-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ffa90-133">System.String</span></span>

## <span data-ttu-id="ffa90-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ffa90-134">OUTPUTS</span></span>

### <span data-ttu-id="ffa90-135">System.Collections.Generic.List<.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="ffa90-135">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="ffa90-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ffa90-136">NOTES</span></span>

## <span data-ttu-id="ffa90-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffa90-137">RELATED LINKS</span></span>

[<span data-ttu-id="ffa90-138">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="ffa90-138">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)