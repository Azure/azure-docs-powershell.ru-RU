---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: eedeeb3311373c240cd564534d3438b948c7a0f6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505839"
---
# <span data-ttu-id="e3c71-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3c71-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="e3c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3c71-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c71-103">Удаляет ImmutabilityPolicy контейнера BLOB-хранилищ с незаблокируемой политикой.</span><span class="sxs-lookup"><span data-stu-id="e3c71-103">Removes ImmutabilityPolicy of a Storage blob container with an unlocked policy</span></span>

## <span data-ttu-id="e3c71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3c71-104">SYNTAX</span></span>

### <span data-ttu-id="e3c71-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3c71-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3c71-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e3c71-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c71-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="e3c71-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c71-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="e3c71-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c71-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3c71-109">DESCRIPTION</span></span>
<span data-ttu-id="e3c71-110">С **помощью cmdlet Remove-AzRmStorageContainerImmutabilityPolicy** удаляется поле ImmutabilityPolicy контейнера BLOB-хранилищ с незаблокируемой политикой.</span><span class="sxs-lookup"><span data-stu-id="e3c71-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob container with an unlocked policy.</span></span>

## <span data-ttu-id="e3c71-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3c71-111">EXAMPLES</span></span>

### <span data-ttu-id="e3c71-112">Пример 1. Удаление незаблокируемого контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="e3c71-112">Example 1: Remove unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="e3c71-113">Эта команда удаляет незаблокируемую блокировку ImmutabilityPolicy контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="e3c71-113">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="e3c71-114">Пример 2. Удаление незаблокируемой политики ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e3c71-114">Example 2: Remove unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="e3c71-115">Эта команда удаляет незаблокируемую блокировку ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e3c71-115">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="e3c71-116">Пример 3. Удаление незаблокируемой политики ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом-контейнером</span><span class="sxs-lookup"><span data-stu-id="e3c71-116">Example 3: Remove unlocked ImmutabilityPolicy of a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="e3c71-117">Эта команда удаляет незаблокируемую блокировку ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом Storage Container.</span><span class="sxs-lookup"><span data-stu-id="e3c71-117">This command removes unlocked ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="e3c71-118">Пример 4. Удаление незаблокируемой политики ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3c71-118">Example 4: Remove unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="e3c71-119">Эта команда удаляет незаблокируемую блокировку ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="e3c71-119">This command removes unlocked ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="e3c71-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3c71-120">PARAMETERS</span></span>

### <span data-ttu-id="e3c71-121">-Container</span><span class="sxs-lookup"><span data-stu-id="e3c71-121">-Container</span></span>
<span data-ttu-id="e3c71-122">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="e3c71-122">Storage container object</span></span>

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

### <span data-ttu-id="e3c71-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="e3c71-123">-ContainerName</span></span>
<span data-ttu-id="e3c71-124">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="e3c71-124">Container Name</span></span>

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

### <span data-ttu-id="e3c71-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c71-125">-DefaultProfile</span></span>
<span data-ttu-id="e3c71-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c71-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c71-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="e3c71-127">-Etag</span></span>
<span data-ttu-id="e3c71-128">Etag политики immutability.</span><span class="sxs-lookup"><span data-stu-id="e3c71-128">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3c71-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3c71-129">-InputObject</span></span>
<span data-ttu-id="e3c71-130">Unlocked ImmutabilityPolicy Object to Remove</span><span class="sxs-lookup"><span data-stu-id="e3c71-130">Unlocked ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3c71-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c71-131">-ResourceGroupName</span></span>
<span data-ttu-id="e3c71-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3c71-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="e3c71-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3c71-133">-StorageAccount</span></span>
<span data-ttu-id="e3c71-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="e3c71-134">Storage account object</span></span>

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

### <span data-ttu-id="e3c71-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e3c71-135">-StorageAccountName</span></span>
<span data-ttu-id="e3c71-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="e3c71-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="e3c71-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3c71-137">-Confirm</span></span>
<span data-ttu-id="e3c71-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c71-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c71-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c71-139">-WhatIf</span></span>
<span data-ttu-id="e3c71-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c71-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c71-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e3c71-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c71-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c71-142">CommonParameters</span></span>
<span data-ttu-id="e3c71-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c71-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c71-144">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c71-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c71-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3c71-145">INPUTS</span></span>

### <span data-ttu-id="e3c71-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e3c71-146">System.String</span></span>

### <span data-ttu-id="e3c71-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e3c71-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="e3c71-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="e3c71-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="e3c71-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3c71-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="e3c71-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3c71-150">OUTPUTS</span></span>

### <span data-ttu-id="e3c71-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="e3c71-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="e3c71-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3c71-152">NOTES</span></span>

## <span data-ttu-id="e3c71-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3c71-153">RELATED LINKS</span></span>
