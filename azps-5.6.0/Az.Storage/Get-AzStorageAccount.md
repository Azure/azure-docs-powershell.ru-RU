---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2c8980f198dc675e12a9b9c6048a4960c1998f9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002808"
---
# <span data-ttu-id="c3d18-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d18-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="c3d18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3d18-102">SYNOPSIS</span></span>
<span data-ttu-id="c3d18-103">Получает учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c3d18-103">Gets a Storage account.</span></span>

## <span data-ttu-id="c3d18-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c3d18-104">SYNTAX</span></span>

### <span data-ttu-id="c3d18-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d18-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c3d18-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d18-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeGeoReplicationStats] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3d18-107">BlobRestoreStatusParameterSet</span><span class="sxs-lookup"><span data-stu-id="c3d18-107">BlobRestoreStatusParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-IncludeBlobRestoreStatus] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3d18-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3d18-108">DESCRIPTION</span></span>
<span data-ttu-id="c3d18-109">Для получения учетной записи **Get-AzStorageAccount** вы получаете указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="c3d18-109">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="c3d18-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c3d18-110">EXAMPLES</span></span>

### <span data-ttu-id="c3d18-111">Пример 1. Получить указанную учетную запись хранения</span><span class="sxs-lookup"><span data-stu-id="c3d18-111">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="c3d18-112">Эта команда получает указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="c3d18-112">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="c3d18-113">Пример 2. Получить все учетные записи хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c3d18-113">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="c3d18-114">Эта команда получает все учетные записи хранения в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3d18-114">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="c3d18-115">Пример 3. Все учетные записи хранения в подписке</span><span class="sxs-lookup"><span data-stu-id="c3d18-115">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="c3d18-116">Эта команда получает все учетные записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="c3d18-116">This command gets all of the Storage accounts in the subscription.</span></span>

### <span data-ttu-id="c3d18-117">Пример 4. Получить учетные записи хранения с состоянием восстановления BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="c3d18-117">Example 4:  Get a Storage accounts with its blob restore status</span></span>
```
PS C:\> $account = Get-AzStorageAccount -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -IncludeBlobRestoreStatus

PS C:\> $account.BlobRestoreStatus

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                 
------     ---------                            ------------- ------------------------     ---------------------                 
InProgress a70cd4a1-f223-4c86-959f-cc13eb4795a8               2020-02-10T13:45:04.7155962Z [container1/blob1 -> container2/blob2]
```

<span data-ttu-id="c3d18-118">Эта команда получает учетные записи хранения с состоянием восстановления BLOB-хранилищ и показывает их состояние.</span><span class="sxs-lookup"><span data-stu-id="c3d18-118">This command gets a Storage accounts with its blob restore status, and show the blob restore status.</span></span>

## <span data-ttu-id="c3d18-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3d18-119">PARAMETERS</span></span>

### <span data-ttu-id="c3d18-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3d18-120">-AsJob</span></span>
<span data-ttu-id="c3d18-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3d18-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3d18-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3d18-122">-DefaultProfile</span></span>
<span data-ttu-id="c3d18-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3d18-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3d18-124">-IncludeBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c3d18-124">-IncludeBlobRestoreStatus</span></span>
<span data-ttu-id="c3d18-125">Получите BlobRestoreStatus учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c3d18-125">Get the BlobRestoreStatus of the Storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3d18-126">-IncludeGeoReplicationStats</span><span class="sxs-lookup"><span data-stu-id="c3d18-126">-IncludeGeoReplicationStats</span></span>
<span data-ttu-id="c3d18-127">Получить geoReplicationStats учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c3d18-127">Get the GeoReplicationStats of the Storage account.</span></span>

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

### <span data-ttu-id="c3d18-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c3d18-128">-Name</span></span>
<span data-ttu-id="c3d18-129">Имя учетной записи хранения, которая нужно получить.</span><span class="sxs-lookup"><span data-stu-id="c3d18-129">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d18-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3d18-130">-ResourceGroupName</span></span>
<span data-ttu-id="c3d18-131">Имя группы ресурсов, которая содержит учетную запись хранения, которую нужно получить.</span><span class="sxs-lookup"><span data-stu-id="c3d18-131">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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
Parameter Sets: AccountNameParameterSet, BlobRestoreStatusParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3d18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3d18-132">CommonParameters</span></span>
<span data-ttu-id="c3d18-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3d18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3d18-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3d18-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3d18-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d18-135">INPUTS</span></span>

### <span data-ttu-id="c3d18-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c3d18-136">System.String</span></span>

## <span data-ttu-id="c3d18-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c3d18-137">OUTPUTS</span></span>

### <span data-ttu-id="c3d18-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d18-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c3d18-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c3d18-139">NOTES</span></span>

## <span data-ttu-id="c3d18-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3d18-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3d18-141">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d18-141">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="c3d18-142">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d18-142">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="c3d18-143">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c3d18-143">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


