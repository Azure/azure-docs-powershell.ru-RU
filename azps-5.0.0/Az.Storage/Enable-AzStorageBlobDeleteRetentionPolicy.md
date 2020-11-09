---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: ebb379217f9fd040aa3dcbd6c614a45dbdbba8c4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249776"
---
# <span data-ttu-id="54450-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54450-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="54450-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54450-102">SYNOPSIS</span></span>
<span data-ttu-id="54450-103">Включите удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="54450-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="54450-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54450-104">SYNTAX</span></span>

### <span data-ttu-id="54450-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54450-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54450-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="54450-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54450-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="54450-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54450-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54450-108">DESCRIPTION</span></span>
<span data-ttu-id="54450-109">Командлет **Enable-AzStorageBlobDeleteRetentionPolicy** включает удаление политики хранения для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="54450-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="54450-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54450-110">EXAMPLES</span></span>

### <span data-ttu-id="54450-111">Пример 1: Включение удаления политики хранения для службы больших двоичных объектов</span><span class="sxs-lookup"><span data-stu-id="54450-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="54450-112">Эта команда включает удаление политики хранения для службы больших двоичных объектов и задает для удаленных дней для хранения BLOB-данных значение 4.</span><span class="sxs-lookup"><span data-stu-id="54450-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="54450-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54450-113">PARAMETERS</span></span>

### <span data-ttu-id="54450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54450-114">-DefaultProfile</span></span>
<span data-ttu-id="54450-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54450-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54450-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54450-116">-PassThru</span></span>
<span data-ttu-id="54450-117">Показать ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="54450-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="54450-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54450-118">-ResourceGroupName</span></span>
<span data-ttu-id="54450-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54450-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="54450-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54450-120">-ResourceId</span></span>
<span data-ttu-id="54450-121">Введите идентификатор ресурса учетной записи хранения или идентификатор ресурса свойств службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="54450-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="54450-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="54450-122">-RetentionDays</span></span>
<span data-ttu-id="54450-123">Задает количество дней хранения для DeleteRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="54450-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

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

### <span data-ttu-id="54450-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="54450-124">-StorageAccount</span></span>
<span data-ttu-id="54450-125">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="54450-125">Storage account object</span></span>

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

### <span data-ttu-id="54450-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="54450-126">-StorageAccountName</span></span>
<span data-ttu-id="54450-127">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="54450-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="54450-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54450-128">-Confirm</span></span>
<span data-ttu-id="54450-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54450-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54450-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54450-130">-WhatIf</span></span>
<span data-ttu-id="54450-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54450-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54450-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54450-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54450-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54450-133">CommonParameters</span></span>
<span data-ttu-id="54450-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54450-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54450-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54450-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54450-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54450-136">INPUTS</span></span>

### <span data-ttu-id="54450-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="54450-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="54450-138">System. String</span><span class="sxs-lookup"><span data-stu-id="54450-138">System.String</span></span>

## <span data-ttu-id="54450-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54450-139">OUTPUTS</span></span>

### <span data-ttu-id="54450-140">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="54450-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="54450-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="54450-141">NOTES</span></span>

## <span data-ttu-id="54450-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54450-142">RELATED LINKS</span></span>