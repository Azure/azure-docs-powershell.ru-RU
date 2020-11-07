---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: a7183498bba029a7b744a45bd34047926da4bf54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728586"
---
# <span data-ttu-id="b233b-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="b233b-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="b233b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b233b-102">SYNOPSIS</span></span>
<span data-ttu-id="b233b-103">Удаляет теги допустимых удержаний из контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="b233b-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="b233b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b233b-104">SYNTAX</span></span>

### <span data-ttu-id="b233b-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b233b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b233b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b233b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b233b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b233b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b233b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b233b-108">DESCRIPTION</span></span>
<span data-ttu-id="b233b-109">Командлет **Remove-AzRmStorageContainerLegalHold** Удаляет теги допустимых удержаний из контейнера BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="b233b-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="b233b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b233b-110">EXAMPLES</span></span>

### <span data-ttu-id="b233b-111">Пример 1. Удалите теги юридических удержаний из контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="b233b-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="b233b-112">Эта команда удаляет Теги допустимых удержаний из контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="b233b-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="b233b-113">Пример 2. Удалите теги юридических удержаний из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="b233b-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="b233b-114">Эта команда удаляет Теги допустимых удержаний из контейнера BLOB-объектов хранилища с объектом учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="b233b-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b233b-115">Пример 3. Удалите теги юридических удержаний из всех контейнеров больших двоичных объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b233b-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="b233b-116">Эта команда удаляет Теги допустимых удержаний из всех контейнеров BLOB-объектов хранилища в учетной записи хранения с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="b233b-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b233b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b233b-117">PARAMETERS</span></span>

### <span data-ttu-id="b233b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="b233b-118">-Container</span></span>
<span data-ttu-id="b233b-119">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="b233b-119">Storage container object</span></span>

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

### <span data-ttu-id="b233b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b233b-120">-DefaultProfile</span></span>
<span data-ttu-id="b233b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b233b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b233b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b233b-122">-Name</span></span>
<span data-ttu-id="b233b-123">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="b233b-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b233b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b233b-124">-ResourceGroupName</span></span>
<span data-ttu-id="b233b-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b233b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b233b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b233b-126">-StorageAccount</span></span>
<span data-ttu-id="b233b-127">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b233b-127">Storage account object</span></span>

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

### <span data-ttu-id="b233b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b233b-128">-StorageAccountName</span></span>
<span data-ttu-id="b233b-129">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b233b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="b233b-130">-Тег</span><span class="sxs-lookup"><span data-stu-id="b233b-130">-Tag</span></span>
<span data-ttu-id="b233b-131">Теги LegalHold контейнеров</span><span class="sxs-lookup"><span data-stu-id="b233b-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b233b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b233b-132">-Confirm</span></span>
<span data-ttu-id="b233b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b233b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b233b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b233b-134">-WhatIf</span></span>
<span data-ttu-id="b233b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b233b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b233b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b233b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b233b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b233b-137">CommonParameters</span></span>
<span data-ttu-id="b233b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b233b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b233b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b233b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b233b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b233b-140">INPUTS</span></span>

### <span data-ttu-id="b233b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b233b-141">System.String</span></span>

### <span data-ttu-id="b233b-142">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b233b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b233b-143">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b233b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b233b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b233b-144">OUTPUTS</span></span>

### <span data-ttu-id="b233b-145">Microsoft. Azure. Commands. Management. Storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="b233b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="b233b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b233b-146">NOTES</span></span>

## <span data-ttu-id="b233b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b233b-147">RELATED LINKS</span></span>
