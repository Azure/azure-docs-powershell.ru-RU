---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: BF0A5D64-AC93-48F5-AED2-C21CC8829053
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 750203e954ef96619e32b63ffd6eae333bb852f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900778"
---
# <span data-ttu-id="6fbe9-101">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="6fbe9-101">Get-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="6fbe9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6fbe9-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbe9-103">Поиск удаленных записей в корзине, соответствующих фильтру.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-103">Searches for deleted entries in trash which match the filter.</span></span>

## <span data-ttu-id="6fbe9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6fbe9-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreDeletedItem [-Account] <String> [-Filter] <String> [-Count <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fbe9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbe9-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbe9-106">Командлет **Get-AzDataLakeStoreDeletedItem** просматривает удаленные файлы или папки в Data Lake Store, которые соответствуют данному фильтру.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-106">The **Get-AzDataLakeStoreDeletedItem** cmdlet searches the deleted files or folders in Data Lake Store which match the given filter.</span></span>
<span data-ttu-id="6fbe9-107">Отображаются следующие атрибуты удаленных элементов: OriginalPath, TrashDirPath, Type, CreationTime.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-107">It displays the following attributes of the deleted items - OriginalPath, TrashDirPath, Type, CreationTime.</span></span>
<span data-ttu-id="6fbe9-108">Это может занять длительное время, так как вам может потребоваться выполнить поиск в миллионах файлов в корзине и запустить ее как задачу.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-108">This could be a long running operation as it may have to search through millions of files in trash and could be run as a job.</span></span>

## <span data-ttu-id="6fbe9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6fbe9-109">EXAMPLES</span></span>

### <span data-ttu-id="6fbe9-110">Пример: получение сведений о файле из Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="6fbe9-110">Example: Get details of a file from the Data Lake Store</span></span>
```
PS> Get-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Filter test0/file_123

TrashDirPath                         OriginalPath                                          Type CreationTime
------------                         ------------                                          ---- ------------
cd6ad5ce-792b-4812-8a33-8f9ed19eb532 adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 FILE 2/8/2019 8:12:18 AM
356cfd42-39c7-451e-96cb-9f47883d91e2 adl://ml1ptrashtest.azuredatalake.com/test0/file_1232 FILE 2/8/2019 8:12:18 AM
e7b30ac8-2dbc-43a3-8ca6-2d420ac0c488 adl://ml1ptrashtest.azuredatalake.com/test0/file_1237 FILE 2/8/2019 8:12:18 AM
```

## <span data-ttu-id="6fbe9-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6fbe9-111">PARAMETERS</span></span>

### <span data-ttu-id="6fbe9-112">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="6fbe9-112">-Account</span></span>
<span data-ttu-id="6fbe9-113">Указывает имя учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6fbe9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fbe9-114">-AsJob</span></span>
<span data-ttu-id="6fbe9-115">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-115">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6fbe9-116">— Количество</span><span class="sxs-lookup"><span data-stu-id="6fbe9-116">-Count</span></span>
<span data-ttu-id="6fbe9-117">Задает количество результатов, которое пользователь хочет найти.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-117">Specifies the number of results the user wants to find.</span></span> <span data-ttu-id="6fbe9-118">Запрос выполняется до тех пор, пока не будет найден результат подсчета или поиск выполняется во всей корзине, где бы они ни были.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-118">The query runs until it finds Count results or it searches through entire trash, whichever happens first.</span></span>

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

### <span data-ttu-id="6fbe9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbe9-119">-DefaultProfile</span></span>
<span data-ttu-id="6fbe9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbe9-121">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="6fbe9-121">-Filter</span></span>
<span data-ttu-id="6fbe9-122">Задает поисковый запрос.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-122">Specifies the search query.</span></span> <span data-ttu-id="6fbe9-123">Более конкретное значение предоставляет более важные результаты.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-123">A more specific value gives more relevant results.</span></span>

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

### <span data-ttu-id="6fbe9-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbe9-124">CommonParameters</span></span>
<span data-ttu-id="6fbe9-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6fbe9-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbe9-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fbe9-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbe9-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6fbe9-127">INPUTS</span></span>

### <span data-ttu-id="6fbe9-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6fbe9-128">System.String</span></span>

## <span data-ttu-id="6fbe9-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbe9-129">OUTPUTS</span></span>

### <span data-ttu-id="6fbe9-130">System. Collections. Generic. List<Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreDeletedItem></span><span class="sxs-lookup"><span data-stu-id="6fbe9-130">System.Collections.Generic.List<Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem></span></span>

## <span data-ttu-id="6fbe9-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6fbe9-131">NOTES</span></span>

## <span data-ttu-id="6fbe9-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fbe9-132">RELATED LINKS</span></span>

[<span data-ttu-id="6fbe9-133">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="6fbe9-133">Restore-AzDataLakeStoreDeletedItem</span></span>](./Restore-AzDataLakeStoreDeletedItem.md)