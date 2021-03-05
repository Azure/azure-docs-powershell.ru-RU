---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: cd3a8b12b6dbd6aec6dbc157aa3ff4d4ce398002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973347"
---
# <span data-ttu-id="48b1b-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="48b1b-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="48b1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="48b1b-103">Включает политику восстановления BLOB-устройств для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="48b1b-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="48b1b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="48b1b-104">SYNTAX</span></span>

### <span data-ttu-id="48b1b-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48b1b-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48b1b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="48b1b-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48b1b-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="48b1b-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48b1b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48b1b-108">DESCRIPTION</span></span>
<span data-ttu-id="48b1b-109">С **помощью cmdlet Enable-AzStorageBlobRestorePolicy** можно включить политику восстановления BLOB-приложений для службы BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="48b1b-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="48b1b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="48b1b-110">EXAMPLES</span></span>

### <span data-ttu-id="48b1b-111">Пример 1. Включает политику восстановления BLOB-хранилищ Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="48b1b-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="48b1b-112">Эта команда сначала включает параметрЫ BLOB-объектов softdelete и changefeed, а затем включает политику восстановления BLOB-объектов, после чего проверяет параметр в свойствах службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="48b1b-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="48b1b-113">У BLOB-службы RestorePolicy.Days должно быть меньше, чем DeleteRetentionPolicy.Days.</span><span class="sxs-lookup"><span data-stu-id="48b1b-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="48b1b-114">Перед тем как включить политику восстановления BLOB-клиентов, необходимо включить политики восстановления BLOB-то и ChangeFeed.</span><span class="sxs-lookup"><span data-stu-id="48b1b-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="48b1b-115">Если параметры softdelete и Changefeed включены, может потребоваться подождать некоторое время, прежде чем включит политику восстановления BLOB-целей.</span><span class="sxs-lookup"><span data-stu-id="48b1b-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="48b1b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48b1b-116">PARAMETERS</span></span>

### <span data-ttu-id="48b1b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48b1b-117">-DefaultProfile</span></span>
<span data-ttu-id="48b1b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48b1b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48b1b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48b1b-119">-PassThru</span></span>
<span data-ttu-id="48b1b-120">Отображение свойств службы</span><span class="sxs-lookup"><span data-stu-id="48b1b-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="48b1b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48b1b-121">-ResourceGroupName</span></span>
<span data-ttu-id="48b1b-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48b1b-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48b1b-123">-ResourceId</span></span>
<span data-ttu-id="48b1b-124">Ввести ИД ресурса учетной записи хранения или свойства службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="48b1b-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="48b1b-125">-RestoreDays</span></span>
<span data-ttu-id="48b1b-126">Определяет количество дней, в течение дня для BLOB-части можно восстановить.</span><span class="sxs-lookup"><span data-stu-id="48b1b-126">Sets the number of days for the blob can be restored..</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="48b1b-127">-StorageAccount</span></span>
<span data-ttu-id="48b1b-128">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="48b1b-128">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48b1b-129">-StorageAccountName</span></span>
<span data-ttu-id="48b1b-130">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="48b1b-130">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48b1b-131">-Confirm</span></span>
<span data-ttu-id="48b1b-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="48b1b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48b1b-133">-WhatIf</span></span>
<span data-ttu-id="48b1b-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48b1b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48b1b-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="48b1b-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48b1b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48b1b-136">CommonParameters</span></span>
<span data-ttu-id="48b1b-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48b1b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48b1b-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48b1b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48b1b-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="48b1b-139">INPUTS</span></span>

### <span data-ttu-id="48b1b-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48b1b-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="48b1b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="48b1b-141">System.String</span></span>

## <span data-ttu-id="48b1b-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="48b1b-142">OUTPUTS</span></span>

### <span data-ttu-id="48b1b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="48b1b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="48b1b-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="48b1b-144">NOTES</span></span>

## <span data-ttu-id="48b1b-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48b1b-145">RELATED LINKS</span></span>
