---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 9503f62667405c8e7a652bffc150a747eadb40f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981491"
---
# <span data-ttu-id="4c9a6-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="4c9a6-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="4c9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9a6-103">Свойства служб для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="4c9a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c9a6-104">SYNTAX</span></span>

### <span data-ttu-id="4c9a6-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c9a6-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c9a6-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4c9a6-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c9a6-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="4c9a6-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c9a6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c9a6-108">DESCRIPTION</span></span>
<span data-ttu-id="4c9a6-109">Для файлов хранилища Azure свойства службы свойства **get-AzStorageFileServiceProperty.**</span><span class="sxs-lookup"><span data-stu-id="4c9a6-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="4c9a6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c9a6-110">EXAMPLES</span></span>

### <span data-ttu-id="4c9a6-111">Пример 1. Получить свойство служб хранилища Azure для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="4c9a6-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 3
```

<span data-ttu-id="4c9a6-112">Эта команда получает свойство служб File services указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="4c9a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c9a6-113">PARAMETERS</span></span>

### <span data-ttu-id="4c9a6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9a6-114">-DefaultProfile</span></span>
<span data-ttu-id="4c9a6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c9a6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c9a6-116">-ResourceGroupName</span></span>
<span data-ttu-id="4c9a6-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c9a6-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c9a6-118">-ResourceId</span></span>
<span data-ttu-id="4c9a6-119">Ввести ИД ресурса учетной записи хранения или свойства ресурса службы файлов.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c9a6-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c9a6-120">-StorageAccount</span></span>
<span data-ttu-id="4c9a6-121">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="4c9a6-121">Storage account object</span></span>

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

### <span data-ttu-id="4c9a6-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c9a6-122">-StorageAccountName</span></span>
<span data-ttu-id="4c9a6-123">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="4c9a6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9a6-124">CommonParameters</span></span>
<span data-ttu-id="4c9a6-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9a6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9a6-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c9a6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9a6-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c9a6-127">INPUTS</span></span>

### <span data-ttu-id="4c9a6-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c9a6-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4c9a6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4c9a6-129">System.String</span></span>

## <span data-ttu-id="4c9a6-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c9a6-130">OUTPUTS</span></span>

### <span data-ttu-id="4c9a6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="4c9a6-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="4c9a6-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c9a6-132">NOTES</span></span>

## <span data-ttu-id="4c9a6-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c9a6-133">RELATED LINKS</span></span>
