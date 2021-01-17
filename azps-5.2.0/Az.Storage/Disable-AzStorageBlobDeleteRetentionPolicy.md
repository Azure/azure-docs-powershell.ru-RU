---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404343"
---
# <span data-ttu-id="8be23-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8be23-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8be23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8be23-102">SYNOPSIS</span></span>
<span data-ttu-id="8be23-103">Отключите политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8be23-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8be23-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8be23-104">SYNTAX</span></span>

### <span data-ttu-id="8be23-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8be23-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be23-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8be23-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8be23-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8be23-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8be23-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8be23-108">DESCRIPTION</span></span>
<span data-ttu-id="8be23-109">Cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** отключает политику хранения удаления для службы BLOB-документов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="8be23-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8be23-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8be23-110">EXAMPLES</span></span>

### <span data-ttu-id="8be23-111">Пример 1. Отключение политики хранения удаления для службы BLOB-документов</span><span class="sxs-lookup"><span data-stu-id="8be23-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="8be23-112">Эта команда отключает политику хранения удаления для службы BLOB-документов.</span><span class="sxs-lookup"><span data-stu-id="8be23-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="8be23-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8be23-113">PARAMETERS</span></span>

### <span data-ttu-id="8be23-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8be23-114">-DefaultProfile</span></span>
<span data-ttu-id="8be23-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8be23-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8be23-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8be23-116">-PassThru</span></span>
<span data-ttu-id="8be23-117">Отображение свойств службы</span><span class="sxs-lookup"><span data-stu-id="8be23-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="8be23-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8be23-118">-ResourceGroupName</span></span>
<span data-ttu-id="8be23-119">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8be23-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8be23-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8be23-120">-ResourceId</span></span>
<span data-ttu-id="8be23-121">Ввести ИД ресурса учетной записи хранения или свойства службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="8be23-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="8be23-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8be23-122">-StorageAccount</span></span>
<span data-ttu-id="8be23-123">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="8be23-123">Storage account object</span></span>

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

### <span data-ttu-id="8be23-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8be23-124">-StorageAccountName</span></span>
<span data-ttu-id="8be23-125">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="8be23-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="8be23-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8be23-126">-Confirm</span></span>
<span data-ttu-id="8be23-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8be23-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8be23-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8be23-128">-WhatIf</span></span>
<span data-ttu-id="8be23-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8be23-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8be23-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8be23-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8be23-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8be23-131">CommonParameters</span></span>
<span data-ttu-id="8be23-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8be23-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8be23-133">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8be23-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8be23-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8be23-134">INPUTS</span></span>

### <span data-ttu-id="8be23-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8be23-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8be23-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8be23-136">System.String</span></span>

## <span data-ttu-id="8be23-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8be23-137">OUTPUTS</span></span>

### <span data-ttu-id="8be23-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="8be23-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="8be23-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8be23-139">NOTES</span></span>

## <span data-ttu-id="8be23-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8be23-140">RELATED LINKS</span></span>
