---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: b7686b57175958ec2ce4bd1466ca111cce219e05
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728588"
---
# <span data-ttu-id="bd757-101">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bd757-101">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="bd757-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bd757-102">SYNOPSIS</span></span>
<span data-ttu-id="bd757-103">Удаляет ImmutabilityPolicy контейнеров BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="bd757-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="bd757-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bd757-104">SYNTAX</span></span>

### <span data-ttu-id="bd757-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd757-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd757-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bd757-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -Etag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd757-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="bd757-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -Etag <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd757-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="bd757-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd757-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd757-109">DESCRIPTION</span></span>
<span data-ttu-id="bd757-110">Командлет **Remove-AzRmStorageContainerImmutabilityPolicy** удаляет ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="bd757-110">The **Remove-AzRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="bd757-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bd757-111">EXAMPLES</span></span>

### <span data-ttu-id="bd757-112">Пример 1: удаление ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="bd757-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="bd757-113">Эта команда удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="bd757-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="bd757-114">Пример 2: удаление ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bd757-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="bd757-115">Эта команда удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd757-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="bd757-116">Пример 3: удаление ImmutabilityPolicyof контейнера BLOB-объектов хранилища с объектом контейнера</span><span class="sxs-lookup"><span data-stu-id="bd757-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="bd757-117">Эта команда удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища.</span><span class="sxs-lookup"><span data-stu-id="bd757-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="bd757-118">Пример 4: удаление ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bd757-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="bd757-119">Эта команда удаляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="bd757-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="bd757-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bd757-120">PARAMETERS</span></span>

### <span data-ttu-id="bd757-121">-Container</span><span class="sxs-lookup"><span data-stu-id="bd757-121">-Container</span></span>
<span data-ttu-id="bd757-122">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="bd757-122">Storage container object</span></span>

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

### <span data-ttu-id="bd757-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="bd757-123">-ContainerName</span></span>
<span data-ttu-id="bd757-124">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="bd757-124">Container Name</span></span>

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

### <span data-ttu-id="bd757-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd757-125">-DefaultProfile</span></span>
<span data-ttu-id="bd757-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd757-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd757-127">-ETag</span><span class="sxs-lookup"><span data-stu-id="bd757-127">-Etag</span></span>
<span data-ttu-id="bd757-128">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="bd757-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="bd757-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd757-129">-InputObject</span></span>
<span data-ttu-id="bd757-130">Объект ImmutabilityPolicy, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="bd757-130">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="bd757-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd757-131">-ResourceGroupName</span></span>
<span data-ttu-id="bd757-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bd757-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd757-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd757-133">-StorageAccount</span></span>
<span data-ttu-id="bd757-134">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="bd757-134">Storage account object</span></span>

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

### <span data-ttu-id="bd757-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bd757-135">-StorageAccountName</span></span>
<span data-ttu-id="bd757-136">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="bd757-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="bd757-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd757-137">-Confirm</span></span>
<span data-ttu-id="bd757-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bd757-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd757-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd757-139">-WhatIf</span></span>
<span data-ttu-id="bd757-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bd757-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd757-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bd757-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd757-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd757-142">CommonParameters</span></span>
<span data-ttu-id="bd757-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bd757-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd757-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd757-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd757-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bd757-145">INPUTS</span></span>

### <span data-ttu-id="bd757-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bd757-146">System.String</span></span>

### <span data-ttu-id="bd757-147">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd757-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bd757-148">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="bd757-148">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="bd757-149">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bd757-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="bd757-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd757-150">OUTPUTS</span></span>

### <span data-ttu-id="bd757-151">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="bd757-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="bd757-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="bd757-152">NOTES</span></span>

## <span data-ttu-id="bd757-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd757-153">RELATED LINKS</span></span>
