---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906981"
---
# <span data-ttu-id="1fdaa-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="1fdaa-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="1fdaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1fdaa-102">SYNOPSIS</span></span>
<span data-ttu-id="1fdaa-103">Изменяет свойства службы для службы больших двоичных объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1fdaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1fdaa-104">SYNTAX</span></span>

### <span data-ttu-id="1fdaa-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fdaa-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fdaa-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1fdaa-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fdaa-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="1fdaa-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fdaa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fdaa-108">DESCRIPTION</span></span>
<span data-ttu-id="1fdaa-109">Командлет **Update-AzStorageBlobServiceProperty** изменяет свойства службы для службы BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="1fdaa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1fdaa-110">EXAMPLES</span></span>

### <span data-ttu-id="1fdaa-111">Пример 1: Настройка службы BLOB-объектов DefaultServiceVersion в 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="1fdaa-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="1fdaa-112">Эта команда задает DefaultServiceVersion для службы больших двоичных объектов в 2018-03-28.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="1fdaa-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1fdaa-113">PARAMETERS</span></span>

### <span data-ttu-id="1fdaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fdaa-114">-DefaultProfile</span></span>
<span data-ttu-id="1fdaa-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fdaa-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="1fdaa-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="1fdaa-117">Версия службы по умолчанию для установки</span><span class="sxs-lookup"><span data-stu-id="1fdaa-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fdaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fdaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="1fdaa-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="1fdaa-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fdaa-120">-ResourceId</span></span>
<span data-ttu-id="1fdaa-121">Введите идентификатор ресурса учетной записи хранения или идентификатор ресурса свойств службы BLOB.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="1fdaa-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1fdaa-122">-StorageAccount</span></span>
<span data-ttu-id="1fdaa-123">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="1fdaa-123">Storage account object</span></span>

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

### <span data-ttu-id="1fdaa-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1fdaa-124">-StorageAccountName</span></span>
<span data-ttu-id="1fdaa-125">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="1fdaa-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fdaa-126">-Confirm</span></span>
<span data-ttu-id="1fdaa-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fdaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fdaa-128">-WhatIf</span></span>
<span data-ttu-id="1fdaa-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fdaa-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fdaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fdaa-131">CommonParameters</span></span>
<span data-ttu-id="1fdaa-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1fdaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fdaa-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fdaa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fdaa-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1fdaa-134">INPUTS</span></span>

### <span data-ttu-id="1fdaa-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1fdaa-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1fdaa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1fdaa-136">System.String</span></span>

## <span data-ttu-id="1fdaa-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fdaa-137">OUTPUTS</span></span>

### <span data-ttu-id="1fdaa-138">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="1fdaa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="1fdaa-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1fdaa-139">NOTES</span></span>

## <span data-ttu-id="1fdaa-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fdaa-140">RELATED LINKS</span></span>
