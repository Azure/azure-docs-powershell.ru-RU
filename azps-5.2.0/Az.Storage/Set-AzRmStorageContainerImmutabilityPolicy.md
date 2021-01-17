---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 9631855803b4ad16312c907c1d1c747b3aee6fdf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403343"
---
# <span data-ttu-id="feb2b-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="feb2b-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="feb2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="feb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="feb2b-103">Создание и обновление ImmutabilityPolicy контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="feb2b-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="feb2b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="feb2b-104">SYNTAX</span></span>

### <span data-ttu-id="feb2b-105">AccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="feb2b-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="feb2b-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-ImmutabilityPeriod <Int32>] [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feb2b-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> [-ImmutabilityPeriod <Int32>]
 [-AllowProtectedAppendWrite <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="feb2b-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb2b-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="feb2b-113">DESCRIPTION</span></span>
<span data-ttu-id="feb2b-114">Cmdlet **Set-AzRmStorageContainerImmutabilityPolicy** создает или обновляет ImmutabilityPolicy контейнеров BLOB-хранилищ.</span><span class="sxs-lookup"><span data-stu-id="feb2b-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="feb2b-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="feb2b-115">EXAMPLES</span></span>

### <span data-ttu-id="feb2b-116">Пример 1. Создание или обновление ImmutabilityPolicy контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера</span><span class="sxs-lookup"><span data-stu-id="feb2b-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="feb2b-117">Эта команда создает или обновляет ImmutabilityPolicy контейнера BLOB-хранилищ с именем учетной записи хранения и именем контейнера.</span><span class="sxs-lookup"><span data-stu-id="feb2b-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="feb2b-118">Пример 2. Расширение ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="feb2b-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="feb2b-119">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="feb2b-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="feb2b-120">Extend ImmutabilityPolicy can run only after ImmutabilityPolicy is locked.</span><span class="sxs-lookup"><span data-stu-id="feb2b-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="feb2b-121">Пример 3. Обновление ImmutabilityPolicy контейнера BLOB-хранилищ</span><span class="sxs-lookup"><span data-stu-id="feb2b-121">Example 3: Update ImmutabilityPolicy of a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -AllowProtectedAppendWrite $true
```

<span data-ttu-id="feb2b-122">Эта команда обновляет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом контейнера хранилища 3 раза: Сначала для ImmutabilityPeriod 12 дней без etag, а для ImmutabilityPeriod 9 дней с etag, наконец, включено AllowProtectedAppendWrite.</span><span class="sxs-lookup"><span data-stu-id="feb2b-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 3 times: First to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag, finally enabled AllowProtectedAppendWrite.</span></span>

### <span data-ttu-id="feb2b-123">Пример 4. Extend ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="feb2b-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="feb2b-124">Эта команда расширяет ImmutabilityPolicy контейнера BLOB-объектов хранилища с объектом ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="feb2b-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="feb2b-125">Extend ImmutabilityPolicy can run only after ImmutabilityPolicy is locked.</span><span class="sxs-lookup"><span data-stu-id="feb2b-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="feb2b-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="feb2b-126">PARAMETERS</span></span>

### <span data-ttu-id="feb2b-127">-AllowProtectedAppendWrite</span><span class="sxs-lookup"><span data-stu-id="feb2b-127">-AllowProtectedAppendWrite</span></span>
<span data-ttu-id="feb2b-128">Это свойство можно изменить только для политик хранения с учетом времени.</span><span class="sxs-lookup"><span data-stu-id="feb2b-128">This property can only be changed for unlocked time-based retention policies.</span></span> <span data-ttu-id="feb2b-129">Если это свойство включено, новые блоки можно писать в объекты-объекты приложения, сохраняя при этом защиту от ненамеренного использования и соответствие требованиям.</span><span class="sxs-lookup"><span data-stu-id="feb2b-129">With this property enabled, new blocks can be written to an append blob while maintaining immutability protection and compliance.</span></span> <span data-ttu-id="feb2b-130">Можно добавлять только новые блоки, а существующие блоки нельзя изменять и удалять.</span><span class="sxs-lookup"><span data-stu-id="feb2b-130">Only new blocks can be added and any existing blocks cannot be modified or deleted.</span></span>

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

### <span data-ttu-id="feb2b-131">-Container</span><span class="sxs-lookup"><span data-stu-id="feb2b-131">-Container</span></span>
<span data-ttu-id="feb2b-132">Объект контейнера хранилища</span><span class="sxs-lookup"><span data-stu-id="feb2b-132">Storage container object</span></span>

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

### <span data-ttu-id="feb2b-133">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="feb2b-133">-ContainerName</span></span>
<span data-ttu-id="feb2b-134">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="feb2b-134">Container Name</span></span>

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

### <span data-ttu-id="feb2b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb2b-135">-DefaultProfile</span></span>
<span data-ttu-id="feb2b-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="feb2b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="feb2b-137">-Etag</span><span class="sxs-lookup"><span data-stu-id="feb2b-137">-Etag</span></span>
<span data-ttu-id="feb2b-138">Etag политики immutability.</span><span class="sxs-lookup"><span data-stu-id="feb2b-138">Immutability policy etag.</span></span> <span data-ttu-id="feb2b-139">Если поле -ExtendPolicy не указано, то Etag является необязательным. иначе требуется Etag.</span><span class="sxs-lookup"><span data-stu-id="feb2b-139">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

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

### <span data-ttu-id="feb2b-140">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="feb2b-140">-ExtendPolicy</span></span>
<span data-ttu-id="feb2b-141">Указать ExtendPolicy для расширения существующего поля ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="feb2b-141">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="feb2b-142">После блокировки ImmutabilityPolicy его можно только продлить.</span><span class="sxs-lookup"><span data-stu-id="feb2b-142">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

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

### <span data-ttu-id="feb2b-143">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="feb2b-143">-ImmutabilityPeriod</span></span>
<span data-ttu-id="feb2b-144">Период неавтеричности с момента создания в днях.</span><span class="sxs-lookup"><span data-stu-id="feb2b-144">Immutability period since creation in days.</span></span>

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

### <span data-ttu-id="feb2b-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="feb2b-145">-InputObject</span></span>
<span data-ttu-id="feb2b-146">Имя контейнера</span><span class="sxs-lookup"><span data-stu-id="feb2b-146">Container Name</span></span>

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

### <span data-ttu-id="feb2b-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feb2b-147">-ResourceGroupName</span></span>
<span data-ttu-id="feb2b-148">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="feb2b-148">Resource Group Name.</span></span>

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

### <span data-ttu-id="feb2b-149">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="feb2b-149">-StorageAccount</span></span>
<span data-ttu-id="feb2b-150">Объект учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="feb2b-150">Storage account object</span></span>

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

### <span data-ttu-id="feb2b-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="feb2b-151">-StorageAccountName</span></span>
<span data-ttu-id="feb2b-152">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="feb2b-152">Storage Account Name.</span></span>

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

### <span data-ttu-id="feb2b-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="feb2b-153">-Confirm</span></span>
<span data-ttu-id="feb2b-154">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feb2b-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb2b-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb2b-155">-WhatIf</span></span>
<span data-ttu-id="feb2b-156">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feb2b-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb2b-157">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="feb2b-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb2b-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb2b-158">CommonParameters</span></span>
<span data-ttu-id="feb2b-159">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feb2b-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb2b-160">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feb2b-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb2b-161">INPUTS</span><span class="sxs-lookup"><span data-stu-id="feb2b-161">INPUTS</span></span>

### <span data-ttu-id="feb2b-162">System.String</span><span class="sxs-lookup"><span data-stu-id="feb2b-162">System.String</span></span>

### <span data-ttu-id="feb2b-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="feb2b-163">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="feb2b-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="feb2b-164">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="feb2b-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="feb2b-165">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="feb2b-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="feb2b-166">OUTPUTS</span></span>

### <span data-ttu-id="feb2b-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="feb2b-167">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="feb2b-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="feb2b-168">NOTES</span></span>

## <span data-ttu-id="feb2b-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="feb2b-169">RELATED LINKS</span></span>
