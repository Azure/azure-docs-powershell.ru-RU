---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080193"
---
# <span data-ttu-id="48406-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="48406-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="48406-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48406-102">SYNOPSIS</span></span>
<span data-ttu-id="48406-103">Включение политики восстановления больших двоичных объектов в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="48406-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="48406-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48406-104">SYNTAX</span></span>

### <span data-ttu-id="48406-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48406-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="48406-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="48406-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48406-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="48406-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48406-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48406-108">DESCRIPTION</span></span>
<span data-ttu-id="48406-109">Командлет **Enable-AzStorageBlobRestorePolicy** включает политику восстановления больших двоичных объектов для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="48406-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="48406-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48406-110">EXAMPLES</span></span>

### <span data-ttu-id="48406-111">Пример 1: Включение политики восстановления больших двоичных объектов для службы BLOB-данных хранилища Azure в учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="48406-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
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

<span data-ttu-id="48406-112">Эта команда сначала включает BLOB-softdelete и changefeed, а затем включает политику восстановления больших двоичных объектов, а затем проверяет параметр в свойствах службы больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="48406-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="48406-113">Служба больших двоичных объектов RestorePolicy. Days должна быть меньше DeleteRetentionPolicy. Days.</span><span class="sxs-lookup"><span data-stu-id="48406-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="48406-114">Перед включением политики восстановления BLOB-объектов необходимо включить softdelete и ChangeFeed BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="48406-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="48406-115">Если softdelete и changefeed только что включены, может потребоваться подождать, пока сервер не сможет обработать параметр, прежде чем включать политику восстановления BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="48406-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="48406-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48406-116">PARAMETERS</span></span>

### <span data-ttu-id="48406-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48406-117">-DefaultProfile</span></span>
<span data-ttu-id="48406-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48406-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48406-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48406-119">-PassThru</span></span>
<span data-ttu-id="48406-120">Показать ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="48406-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="48406-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48406-121">-ResourceGroupName</span></span>
<span data-ttu-id="48406-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="48406-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="48406-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="48406-123">-ResourceId</span></span>
<span data-ttu-id="48406-124">Введите идентификатор ресурса учетной записи хранения или идентификатор ресурса свойств службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="48406-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="48406-125">-RestoreDays</span><span class="sxs-lookup"><span data-stu-id="48406-125">-RestoreDays</span></span>
<span data-ttu-id="48406-126">Задает количество дней, в течение которых может быть восстановлен большой двоичный объект.</span><span class="sxs-lookup"><span data-stu-id="48406-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="48406-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="48406-127">-StorageAccount</span></span>
<span data-ttu-id="48406-128">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="48406-128">Storage account object</span></span>

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

### <span data-ttu-id="48406-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48406-129">-StorageAccountName</span></span>
<span data-ttu-id="48406-130">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="48406-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="48406-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48406-131">-Confirm</span></span>
<span data-ttu-id="48406-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="48406-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48406-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48406-133">-WhatIf</span></span>
<span data-ttu-id="48406-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="48406-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48406-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="48406-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48406-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48406-136">CommonParameters</span></span>
<span data-ttu-id="48406-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48406-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48406-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48406-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48406-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48406-139">INPUTS</span></span>

### <span data-ttu-id="48406-140">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="48406-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="48406-141">System. String</span><span class="sxs-lookup"><span data-stu-id="48406-141">System.String</span></span>

## <span data-ttu-id="48406-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48406-142">OUTPUTS</span></span>

### <span data-ttu-id="48406-143">Microsoft. Azure. Commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="48406-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="48406-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="48406-144">NOTES</span></span>

## <span data-ttu-id="48406-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48406-145">RELATED LINKS</span></span>
