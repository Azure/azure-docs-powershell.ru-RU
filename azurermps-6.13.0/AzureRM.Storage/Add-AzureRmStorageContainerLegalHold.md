---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558196"
---
# <span data-ttu-id="946d0-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="946d0-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="946d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="946d0-102">SYNOPSIS</span></span>
<span data-ttu-id="946d0-103">Добавляет теги юридических удержаний в контейнер BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="946d0-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="946d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="946d0-104">SYNTAX</span></span>

### <span data-ttu-id="946d0-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="946d0-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="946d0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="946d0-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="946d0-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="946d0-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="946d0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="946d0-108">DESCRIPTION</span></span>
<span data-ttu-id="946d0-109">Командлет **Add-AzureRmStorageContainerLegalHold** добавляет теги юридических удержаний в контейнер BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="946d0-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="946d0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="946d0-110">EXAMPLES</span></span>

### <span data-ttu-id="946d0-111">Пример 1: Добавление тегов юридических удержаний в контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="946d0-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="946d0-112">Эта команда добавляет теги юридического удержания в контейнер BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="946d0-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="946d0-113">Пример 2. Добавление тегов юридических удержаний в контейнер BLOB-объектов хранилища с помощью объекта учетной записи хранения и имени контейнера</span><span class="sxs-lookup"><span data-stu-id="946d0-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="946d0-114">Эта команда добавляет теги юридического удержания в контейнер BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="946d0-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="946d0-115">Пример 3: Добавление тегов юридического удержания ко всем контейнерам больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="946d0-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="946d0-116">Эта команда добавляет теги юридического удержания ко всем контейнерам больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="946d0-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="946d0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="946d0-117">PARAMETERS</span></span>

### <span data-ttu-id="946d0-118">-Container</span><span class="sxs-lookup"><span data-stu-id="946d0-118">-Container</span></span>
<span data-ttu-id="946d0-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="946d0-119">Storage container object</span></span>

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

### <span data-ttu-id="946d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="946d0-120">-DefaultProfile</span></span>
<span data-ttu-id="946d0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="946d0-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="946d0-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="946d0-122">-Name</span></span>
<span data-ttu-id="946d0-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="946d0-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="946d0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="946d0-124">-ResourceGroupName</span></span>
<span data-ttu-id="946d0-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="946d0-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="946d0-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="946d0-126">-StorageAccount</span></span>
<span data-ttu-id="946d0-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="946d0-127">Storage account object</span></span>

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

### <span data-ttu-id="946d0-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="946d0-128">-StorageAccountName</span></span>
<span data-ttu-id="946d0-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="946d0-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="946d0-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="946d0-130">-Tag</span></span>
<span data-ttu-id="946d0-131">Теги LegalHold контейнеров</span><span class="sxs-lookup"><span data-stu-id="946d0-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946d0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="946d0-132">-Confirm</span></span>
<span data-ttu-id="946d0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="946d0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946d0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="946d0-134">-WhatIf</span></span>
<span data-ttu-id="946d0-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="946d0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="946d0-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="946d0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="946d0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="946d0-137">CommonParameters</span></span>
<span data-ttu-id="946d0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="946d0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="946d0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="946d0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="946d0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="946d0-140">INPUTS</span></span>

### <span data-ttu-id="946d0-141">System. String</span><span class="sxs-lookup"><span data-stu-id="946d0-141">System.String</span></span>

## <span data-ttu-id="946d0-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="946d0-142">OUTPUTS</span></span>

### <span data-ttu-id="946d0-143">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="946d0-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="946d0-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="946d0-144">NOTES</span></span>

## <span data-ttu-id="946d0-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="946d0-145">RELATED LINKS</span></span>

