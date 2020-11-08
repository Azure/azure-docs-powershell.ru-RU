---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: db0c0672a6f60aa8c46f85a98e74f5184842cd72
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066769"
---
# <span data-ttu-id="bd85f-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd85f-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="bd85f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd85f-102">SYNOPSIS</span></span>
<span data-ttu-id="bd85f-103">Получение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd85f-103">Gets a Storage account.</span></span>

## <span data-ttu-id="bd85f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd85f-104">SYNTAX</span></span>

### <span data-ttu-id="bd85f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd85f-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd85f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd85f-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd85f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd85f-107">DESCRIPTION</span></span>
<span data-ttu-id="bd85f-108">Командлет **Get-AzStorageAccount** получает указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="bd85f-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="bd85f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd85f-109">EXAMPLES</span></span>

### <span data-ttu-id="bd85f-110">Пример 1: получение указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bd85f-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="bd85f-111">Эта команда получает указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="bd85f-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="bd85f-112">Пример 2: получение всех учетных записей хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bd85f-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="bd85f-113">Эта команда получает все учетные записи хранения в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd85f-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="bd85f-114">Пример 3: получение всех учетных записей хранения в подписке</span><span class="sxs-lookup"><span data-stu-id="bd85f-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="bd85f-115">Эта команда получает все учетные записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="bd85f-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="bd85f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd85f-116">PARAMETERS</span></span>

### <span data-ttu-id="bd85f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd85f-117">-DefaultProfile</span></span>
<span data-ttu-id="bd85f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd85f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd85f-119">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="bd85f-119">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="bd85f-120">Получить GeoReplicationStats учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd85f-120">Get the GeoReplicationStats of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd85f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bd85f-121">-Name</span></span>
<span data-ttu-id="bd85f-122">Указывает имя учетной записи хранения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bd85f-122">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd85f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd85f-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd85f-124">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="bd85f-124">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd85f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd85f-125">CommonParameters</span></span>
<span data-ttu-id="bd85f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd85f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd85f-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd85f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd85f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd85f-128">INPUTS</span></span>

### <span data-ttu-id="bd85f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bd85f-129">System.String</span></span>

## <span data-ttu-id="bd85f-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd85f-130">OUTPUTS</span></span>

### <span data-ttu-id="bd85f-131">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd85f-131">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="bd85f-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd85f-132">NOTES</span></span>

## <span data-ttu-id="bd85f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd85f-133">RELATED LINKS</span></span>

[<span data-ttu-id="bd85f-134">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd85f-134">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="bd85f-135">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd85f-135">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="bd85f-136">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd85f-136">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


