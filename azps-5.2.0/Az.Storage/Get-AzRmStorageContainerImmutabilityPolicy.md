---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404276"
---
# <span data-ttu-id="d3f3a-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3f3a-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d3f3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f3a-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f3a-103">Gets ImmutabilityPolicy of a Storage BLOB containers</span><span class="sxs-lookup"><span data-stu-id="d3f3a-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d3f3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d3f3a-104">SYNTAX</span></span>

### <span data-ttu-id="d3f3a-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d3f3a-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f3a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d3f3a-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3f3a-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d3f3a-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f3a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3f3a-108">DESCRIPTION</span></span>
<span data-ttu-id="d3f3a-109">**Cmdlet Get-AzRmStorageContainerImmutabilityPolicy** получает ImmutabilityPolicy контейнеров BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="d3f3a-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d3f3a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d3f3a-110">EXAMPLES</span></span>

### <span data-ttu-id="d3f3a-111">Пример 1. Get ImmutabilityPolicy контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="d3f3a-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="d3f3a-112">Эта команда получает ImmutabilityPolicy контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d3f3a-113">Пример 2. Get ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="d3f3a-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="d3f3a-114">Эта команда получает ImmutabilityPolicy контейнеров BLOB-объектов хранилища с именем объекта учетной записи хранения и контейнера.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="d3f3a-115">Пример 3. Get ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом Storage Container</span><span class="sxs-lookup"><span data-stu-id="d3f3a-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="d3f3a-116">Эта команда получает ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом Storage Container.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="d3f3a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f3a-117">PARAMETERS</span></span>

### <span data-ttu-id="d3f3a-118">-Container</span><span class="sxs-lookup"><span data-stu-id="d3f3a-118">-Container</span></span>
<span data-ttu-id="d3f3a-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="d3f3a-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d3f3a-120">-ContainerName</span></span>
<span data-ttu-id="d3f3a-121">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="d3f3a-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f3a-122">-DefaultProfile</span></span>
<span data-ttu-id="d3f3a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f3a-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="d3f3a-124">-Etag</span></span>
<span data-ttu-id="d3f3a-125">Etag политики immutability.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3f3a-126">-ResourceGroupName</span></span>
<span data-ttu-id="d3f3a-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3f3a-128">-StorageAccount</span></span>
<span data-ttu-id="d3f3a-129">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="d3f3a-129">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d3f3a-130">-StorageAccountName</span></span>
<span data-ttu-id="d3f3a-131">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-131">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3f3a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f3a-132">CommonParameters</span></span>
<span data-ttu-id="d3f3a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f3a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f3a-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f3a-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f3a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f3a-135">INPUTS</span></span>

### <span data-ttu-id="d3f3a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d3f3a-136">System.String</span></span>

### <span data-ttu-id="d3f3a-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d3f3a-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d3f3a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="d3f3a-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d3f3a-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3f3a-139">OUTPUTS</span></span>

### <span data-ttu-id="d3f3a-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d3f3a-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d3f3a-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d3f3a-141">NOTES</span></span>

## <span data-ttu-id="d3f3a-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3f3a-142">RELATED LINKS</span></span>
