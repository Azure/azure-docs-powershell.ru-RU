---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: 9a4afaa1a67d9f1f9bffa0fdf6c7b40c7cf72b13
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973379"
---
# <span data-ttu-id="d7594-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d7594-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="d7594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7594-102">SYNOPSIS</span></span>
<span data-ttu-id="d7594-103">В этой области можно включить политику хранения для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="d7594-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d7594-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7594-104">SYNTAX</span></span>

### <span data-ttu-id="d7594-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7594-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7594-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d7594-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7594-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d7594-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7594-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7594-108">DESCRIPTION</span></span>
<span data-ttu-id="d7594-109">С **помощью cmdlet Enable-AzStorageBlobDeleteRetentionPolicy** можно удалить политику хранения для службы BLOB-хранилищ Azure.</span><span class="sxs-lookup"><span data-stu-id="d7594-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d7594-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7594-110">EXAMPLES</span></span>

### <span data-ttu-id="d7594-111">Пример 1. Включить политику хранения для службы BLOB-lob</span><span class="sxs-lookup"><span data-stu-id="d7594-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="d7594-112">Эта команда позволяет удалить политику хранения для службы BLOB-документов и установить для удаленных дней хранения BLOB-4 дней.</span><span class="sxs-lookup"><span data-stu-id="d7594-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="d7594-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7594-113">PARAMETERS</span></span>

### <span data-ttu-id="d7594-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7594-114">-DefaultProfile</span></span>
<span data-ttu-id="d7594-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7594-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7594-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7594-116">-PassThru</span></span>
<span data-ttu-id="d7594-117">Отображение свойств службы</span><span class="sxs-lookup"><span data-stu-id="d7594-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="d7594-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7594-118">-ResourceGroupName</span></span>
<span data-ttu-id="d7594-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7594-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d7594-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d7594-120">-ResourceId</span></span>
<span data-ttu-id="d7594-121">Ввести ИД ресурса учетной записи хранения или свойства службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="d7594-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="d7594-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="d7594-122">-RetentionDays</span></span>
<span data-ttu-id="d7594-123">Определяет количество дней хранения для политики DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="d7594-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="d7594-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7594-124">-StorageAccount</span></span>
<span data-ttu-id="d7594-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d7594-125">Storage account object</span></span>

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

### <span data-ttu-id="d7594-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7594-126">-StorageAccountName</span></span>
<span data-ttu-id="d7594-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d7594-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="d7594-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7594-128">-Confirm</span></span>
<span data-ttu-id="d7594-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d7594-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7594-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7594-130">-WhatIf</span></span>
<span data-ttu-id="d7594-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7594-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7594-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d7594-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7594-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7594-133">CommonParameters</span></span>
<span data-ttu-id="d7594-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7594-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7594-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7594-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7594-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7594-136">INPUTS</span></span>

### <span data-ttu-id="d7594-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d7594-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d7594-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d7594-138">System.String</span></span>

## <span data-ttu-id="d7594-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7594-139">OUTPUTS</span></span>

### <span data-ttu-id="d7594-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d7594-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="d7594-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7594-141">NOTES</span></span>

## <span data-ttu-id="d7594-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7594-142">RELATED LINKS</span></span>
