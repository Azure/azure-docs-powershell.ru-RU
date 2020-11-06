---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568113"
---
# <span data-ttu-id="9e2b0-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2b0-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="9e2b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e2b0-102">SYNOPSIS</span></span>
<span data-ttu-id="9e2b0-103">Возвращает ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e2b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e2b0-104">SYNTAX</span></span>

### <span data-ttu-id="9e2b0-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e2b0-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2b0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9e2b0-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e2b0-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9e2b0-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e2b0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e2b0-108">DESCRIPTION</span></span>
<span data-ttu-id="9e2b0-109">Командлет **Get-AzureRmStorageContainerImmutabilityPolicy** получает ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="9e2b0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e2b0-110">EXAMPLES</span></span>

### <span data-ttu-id="9e2b0-111">Пример 1: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="9e2b0-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="9e2b0-112">Эта команда возвращает ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="9e2b0-113">Пример 2: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="9e2b0-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="9e2b0-114">Эта команда возвращает ImmutabilityPolicy контейнеров BLOB-объектов хранилища с объектом учетной записи хранилища и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="9e2b0-115">Пример 3: получение ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="9e2b0-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="9e2b0-116">Эта команда возвращает ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="9e2b0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e2b0-117">PARAMETERS</span></span>

### <span data-ttu-id="9e2b0-118">-Container</span><span class="sxs-lookup"><span data-stu-id="9e2b0-118">-Container</span></span>
<span data-ttu-id="9e2b0-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="9e2b0-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9e2b0-120">-ContainerName</span></span>
<span data-ttu-id="9e2b0-121">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="9e2b0-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e2b0-122">-DefaultProfile</span></span>
<span data-ttu-id="9e2b0-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="9e2b0-124">-Etag</span></span>
<span data-ttu-id="9e2b0-125">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e2b0-126">-ResourceGroupName</span></span>
<span data-ttu-id="9e2b0-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9e2b0-128">-StorageAccount</span></span>
<span data-ttu-id="9e2b0-129">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9e2b0-129">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9e2b0-130">-StorageAccountName</span></span>
<span data-ttu-id="9e2b0-131">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-131">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e2b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e2b0-132">CommonParameters</span></span>
<span data-ttu-id="9e2b0-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e2b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e2b0-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e2b0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e2b0-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e2b0-135">INPUTS</span></span>

### <span data-ttu-id="9e2b0-136">System. String</span><span class="sxs-lookup"><span data-stu-id="9e2b0-136">System.String</span></span>

## <span data-ttu-id="9e2b0-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e2b0-137">OUTPUTS</span></span>

### <span data-ttu-id="9e2b0-138">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="9e2b0-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="9e2b0-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e2b0-139">NOTES</span></span>

## <span data-ttu-id="9e2b0-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e2b0-140">RELATED LINKS</span></span>

