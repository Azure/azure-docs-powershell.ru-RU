---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249768"
---
# <span data-ttu-id="e18ac-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e18ac-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="e18ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e18ac-102">SYNOPSIS</span></span>
<span data-ttu-id="e18ac-103">Возвращает ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="e18ac-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="e18ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e18ac-104">SYNTAX</span></span>

### <span data-ttu-id="e18ac-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e18ac-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e18ac-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e18ac-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e18ac-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e18ac-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e18ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18ac-108">DESCRIPTION</span></span>
<span data-ttu-id="e18ac-109">Командлет **Get-AzRmStorageContainerImmutabilityPolicy** получает ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="e18ac-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="e18ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e18ac-110">EXAMPLES</span></span>

### <span data-ttu-id="e18ac-111">Пример 1: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="e18ac-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="e18ac-112">Эта команда возвращает ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e18ac-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e18ac-113">Пример 2: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="e18ac-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="e18ac-114">Эта команда возвращает ImmutabilityPolicy контейнеров BLOB-объектов хранилища с объектом учетной записи хранилища и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e18ac-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="e18ac-115">Пример 3: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="e18ac-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="e18ac-116">Эта команда возвращает ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="e18ac-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="e18ac-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e18ac-117">PARAMETERS</span></span>

### <span data-ttu-id="e18ac-118">-Container</span><span class="sxs-lookup"><span data-stu-id="e18ac-118">-Container</span></span>
<span data-ttu-id="e18ac-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="e18ac-119">Storage container object</span></span>

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

### <span data-ttu-id="e18ac-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e18ac-120">-ContainerName</span></span>
<span data-ttu-id="e18ac-121">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="e18ac-121">Container Name</span></span>

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

### <span data-ttu-id="e18ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18ac-122">-DefaultProfile</span></span>
<span data-ttu-id="e18ac-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e18ac-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e18ac-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="e18ac-124">-Etag</span></span>
<span data-ttu-id="e18ac-125">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="e18ac-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="e18ac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18ac-126">-ResourceGroupName</span></span>
<span data-ttu-id="e18ac-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e18ac-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e18ac-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ac-128">-StorageAccount</span></span>
<span data-ttu-id="e18ac-129">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e18ac-129">Storage account object</span></span>

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

### <span data-ttu-id="e18ac-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e18ac-130">-StorageAccountName</span></span>
<span data-ttu-id="e18ac-131">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e18ac-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="e18ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18ac-132">CommonParameters</span></span>
<span data-ttu-id="e18ac-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e18ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18ac-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e18ac-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18ac-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e18ac-135">INPUTS</span></span>

### <span data-ttu-id="e18ac-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e18ac-136">System.String</span></span>

### <span data-ttu-id="e18ac-137">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e18ac-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e18ac-138">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="e18ac-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e18ac-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e18ac-139">OUTPUTS</span></span>

### <span data-ttu-id="e18ac-140">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e18ac-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="e18ac-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e18ac-141">NOTES</span></span>

## <span data-ttu-id="e18ac-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e18ac-142">RELATED LINKS</span></span>
