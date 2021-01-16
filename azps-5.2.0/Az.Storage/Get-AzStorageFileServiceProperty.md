---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324971"
---
# <span data-ttu-id="a63c3-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="a63c3-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="a63c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a63c3-102">SYNOPSIS</span></span>
<span data-ttu-id="a63c3-103">Свойства служб для служб хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="a63c3-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="a63c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a63c3-104">SYNTAX</span></span>

### <span data-ttu-id="a63c3-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a63c3-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a63c3-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a63c3-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a63c3-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="a63c3-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a63c3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a63c3-108">DESCRIPTION</span></span>
<span data-ttu-id="a63c3-109">Для файлов хранилища Azure свойства службы свойства **get-AzStorageFileServiceProperty.**</span><span class="sxs-lookup"><span data-stu-id="a63c3-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="a63c3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a63c3-110">EXAMPLES</span></span>

### <span data-ttu-id="a63c3-111">Пример 1. Получить свойство служб хранилища Azure для указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a63c3-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="a63c3-112">Эта команда получает свойство служб File services указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a63c3-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="a63c3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a63c3-113">PARAMETERS</span></span>

### <span data-ttu-id="a63c3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a63c3-114">-DefaultProfile</span></span>
<span data-ttu-id="a63c3-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a63c3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a63c3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a63c3-116">-ResourceGroupName</span></span>
<span data-ttu-id="a63c3-117">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a63c3-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="a63c3-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a63c3-118">-ResourceId</span></span>
<span data-ttu-id="a63c3-119">Ввести ИД ресурса учетной записи хранения или свойства ресурса службы файлов.</span><span class="sxs-lookup"><span data-stu-id="a63c3-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="a63c3-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a63c3-120">-StorageAccount</span></span>
<span data-ttu-id="a63c3-121">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="a63c3-121">Storage account object</span></span>

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

### <span data-ttu-id="a63c3-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a63c3-122">-StorageAccountName</span></span>
<span data-ttu-id="a63c3-123">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="a63c3-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="a63c3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a63c3-124">CommonParameters</span></span>
<span data-ttu-id="a63c3-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a63c3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a63c3-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a63c3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a63c3-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a63c3-127">INPUTS</span></span>

### <span data-ttu-id="a63c3-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a63c3-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="a63c3-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a63c3-129">System.String</span></span>

## <span data-ttu-id="a63c3-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a63c3-130">OUTPUTS</span></span>

### <span data-ttu-id="a63c3-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="a63c3-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="a63c3-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a63c3-132">NOTES</span></span>

## <span data-ttu-id="a63c3-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a63c3-133">RELATED LINKS</span></span>