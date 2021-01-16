---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 7cdef2f35180712d0751149a85e4a422a868c389
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98418783"
---
# <span data-ttu-id="836e0-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="836e0-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="836e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="836e0-102">SYNOPSIS</span></span>
<span data-ttu-id="836e0-103">Свойства служб для служб BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="836e0-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="836e0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="836e0-104">SYNTAX</span></span>

### <span data-ttu-id="836e0-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="836e0-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="836e0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="836e0-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="836e0-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="836e0-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="836e0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="836e0-108">DESCRIPTION</span></span>
<span data-ttu-id="836e0-109">**Cmdlet Get-AzStorageBlobServiceProperty** возвращает свойства службы для служб BLOB-объектов хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="836e0-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="836e0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="836e0-110">EXAMPLES</span></span>

### <span data-ttu-id="836e0-111">Пример 1. Получить свойство служб BLOB-объектов хранилища Azure для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="836e0-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="836e0-112">Эта команда получает свойство служб BLOB-объектов указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="836e0-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="836e0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="836e0-113">PARAMETERS</span></span>

### <span data-ttu-id="836e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="836e0-114">-DefaultProfile</span></span>
<span data-ttu-id="836e0-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="836e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="836e0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="836e0-116">-ResourceGroupName</span></span>
<span data-ttu-id="836e0-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="836e0-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="836e0-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="836e0-118">-ResourceId</span></span>
<span data-ttu-id="836e0-119">ИД ресурса свойств службы BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="836e0-119">Blob Service Properties Resource Id.</span></span>

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

### <span data-ttu-id="836e0-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="836e0-120">-StorageAccount</span></span>
<span data-ttu-id="836e0-121">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="836e0-121">Storage account object</span></span>

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

### <span data-ttu-id="836e0-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="836e0-122">-StorageAccountName</span></span>
<span data-ttu-id="836e0-123">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="836e0-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="836e0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="836e0-124">CommonParameters</span></span>
<span data-ttu-id="836e0-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="836e0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="836e0-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="836e0-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="836e0-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="836e0-127">INPUTS</span></span>

### <span data-ttu-id="836e0-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="836e0-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="836e0-129">System.String</span><span class="sxs-lookup"><span data-stu-id="836e0-129">System.String</span></span>

## <span data-ttu-id="836e0-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="836e0-130">OUTPUTS</span></span>

### <span data-ttu-id="836e0-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="836e0-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="836e0-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="836e0-132">NOTES</span></span>

## <span data-ttu-id="836e0-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="836e0-133">RELATED LINKS</span></span>
