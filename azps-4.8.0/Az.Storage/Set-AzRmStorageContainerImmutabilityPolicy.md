---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243789"
---
# <span data-ttu-id="ed737-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed737-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ed737-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed737-102">SYNOPSIS</span></span>
<span data-ttu-id="ed737-103">Создание или обновление ImmutabilityPolicy контейнеров BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="ed737-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="ed737-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed737-104">SYNTAX</span></span>

### <span data-ttu-id="ed737-105">Имя_учетной_записи (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ed737-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="ed737-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ed737-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="ed737-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ed737-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="ed737-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed737-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ed737-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed737-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ed737-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed737-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed737-113">DESCRIPTION</span></span>
<span data-ttu-id="ed737-114">Командлет **Set-AzRmStorageContainerImmutabilityPolicy** создает или обновляет ImmutabilityPolicy контейнеров BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="ed737-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="ed737-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed737-115">EXAMPLES</span></span>

### <span data-ttu-id="ed737-116">Пример 1: создание или обновление ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="ed737-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="ed737-117">Эта команда создает или обновляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="ed737-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ed737-118">Пример 2: Расширьте ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ed737-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="ed737-119">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища, используя объект учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ed737-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="ed737-120">Extend ImmutabilityPolicy можно запускать только после блокировки ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed737-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="ed737-121">Пример 3: обновление ImmutabilityPolicy контейнера BLOB-объектов хранилища</span><span class="sxs-lookup"><span data-stu-id="ed737-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="ed737-122">Эта команда обновляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища 3 повременны: сначала на ImmutabilityPeriod 12 дней без eTag, а затем на ImmutabilityPeriod 9 дней с ETag, а затем включите AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="ed737-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="ed737-123">Пример 4: продление ImmutabilityPolicy контейнера BLOB-объектов хранилища с помощью объекта ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed737-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="ed737-124">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища с помощью объекта ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed737-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="ed737-125">Extend ImmutabilityPolicy можно запускать только после блокировки ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed737-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="ed737-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed737-126">PARAMETERS</span></span>

### <span data-ttu-id="ed737-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="ed737-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="ed737-128">Это свойство можно изменить только для незаблокированных политик хранения на основе времени.</span><span class="sxs-lookup"><span data-stu-id="ed737-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="ed737-129">Если это свойство включено, новые блоки могут быть написаны в объекте для добавления, сохраняя при этом защиту и соответствие неизменности.</span><span class="sxs-lookup"><span data-stu-id="ed737-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="ed737-130">Можно добавлять только новые блоки и любые существующие блоки, которые нельзя изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="ed737-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-131">-Container</span><span class="sxs-lookup"><span data-stu-id="ed737-131">-Container</span></span>
<span data-ttu-id="ed737-132">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="ed737-132">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ed737-133">-ContainerName</span></span>
<span data-ttu-id="ed737-134">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="ed737-134">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed737-135">-DefaultProfile</span></span>
<span data-ttu-id="ed737-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ed737-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed737-137">-ETag</span><span class="sxs-lookup"><span data-stu-id="ed737-137">-Etag</span></span>
<span data-ttu-id="ed737-138">ETag политики неизменности.</span><span class="sxs-lookup"><span data-stu-id="ed737-138">Immutability policy etag.</span></span> <span data-ttu-id="ed737-139">Если аргумент-ExtendPolicy не указан, ETag является необязательным; требуется другой ETag.</span><span class="sxs-lookup"><span data-stu-id="ed737-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="ed737-140">-ExtendPolicy</span></span>
<span data-ttu-id="ed737-141">Указание ExtendPolicy для продления существующего ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="ed737-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="ed737-142">После того как ImmutabilityPolicy блокируется, он может быть только продлен.</span><span class="sxs-lookup"><span data-stu-id="ed737-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="ed737-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="ed737-144">Период неизменности с момента создания в днях.</span><span class="sxs-lookup"><span data-stu-id="ed737-144">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: AccountName, AccountObject, ContainerObject, ImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed737-145">-InputObject</span></span>
<span data-ttu-id="ed737-146">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="ed737-146">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed737-147">-ResourceGroupName</span></span>
<span data-ttu-id="ed737-148">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed737-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed737-149">-StorageAccount</span></span>
<span data-ttu-id="ed737-150">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ed737-150">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed737-151">-StorageAccountName</span></span>
<span data-ttu-id="ed737-152">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ed737-152">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed737-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ed737-153">-Confirm</span></span>
<span data-ttu-id="ed737-154">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ed737-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed737-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed737-155">-WhatIf</span></span>
<span data-ttu-id="ed737-156">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ed737-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed737-157">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ed737-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed737-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed737-158">CommonParameters</span></span>
<span data-ttu-id="ed737-159">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed737-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed737-160">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed737-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed737-161">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed737-161">INPUTS</span></span>

### <span data-ttu-id="ed737-162">System. String</span><span class="sxs-lookup"><span data-stu-id="ed737-162">System.String</span></span>

### <span data-ttu-id="ed737-163">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ed737-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="ed737-164">Microsoft. Azure. Commands. Management. Storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="ed737-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="ed737-165">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed737-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ed737-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed737-166">OUTPUTS</span></span>

### <span data-ttu-id="ed737-167">Microsoft. Azure. Commands. Management. Storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ed737-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ed737-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed737-168">NOTES</span></span>

## <span data-ttu-id="ed737-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed737-169">RELATED LINKS</span></span>
