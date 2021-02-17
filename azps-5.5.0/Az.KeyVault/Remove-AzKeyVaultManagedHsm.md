---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234052"
---
# <span data-ttu-id="7b26b-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7b26b-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="7b26b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b26b-102">SYNOPSIS</span></span>
<span data-ttu-id="7b26b-103">Удаляет управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="7b26b-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="7b26b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b26b-104">SYNTAX</span></span>

### <span data-ttu-id="7b26b-105">RemoveManagedHsmByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b26b-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b26b-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="7b26b-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b26b-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b26b-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b26b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b26b-108">DESCRIPTION</span></span>
<span data-ttu-id="7b26b-109">**Cmdlet Remove-AzKeyVaultManagedHsm** удаляет указанный управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="7b26b-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="7b26b-110">При этом также удаляются все ключи, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="7b26b-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="7b26b-111">Обратите внимание, что несмотря на то, что для этого cmdlet не требуется указывать группу ресурсов, это необходимо для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="7b26b-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="7b26b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b26b-112">EXAMPLES</span></span>

### <span data-ttu-id="7b26b-113">Пример 1. Удаление управляемой HSM</span><span class="sxs-lookup"><span data-stu-id="7b26b-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="7b26b-114">Эта команда удаляет управляемый хэштег myhsm из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="7b26b-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="7b26b-115">Пример 2. Удаление управляемого hsm из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7b26b-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="7b26b-116">Эта команда удаляет управляемый мигм с именем myhsm из группы ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="7b26b-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="7b26b-117">Если имя группы ресурсов не указано, выполняется поиск управляемой HSM-службы, удаляемой в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7b26b-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="7b26b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b26b-118">PARAMETERS</span></span>

### <span data-ttu-id="7b26b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b26b-119">-AsJob</span></span>
<span data-ttu-id="7b26b-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7b26b-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b26b-121">-DefaultProfile</span></span>
<span data-ttu-id="7b26b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b26b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b26b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="7b26b-123">-Force</span></span>
<span data-ttu-id="7b26b-124">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="7b26b-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="7b26b-125">По умолчанию этот cmdlet запросит подтверждение удаления управляемой HSM-темы.</span><span class="sxs-lookup"><span data-stu-id="7b26b-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b26b-126">-InputObject</span></span>
<span data-ttu-id="7b26b-127">Управляемый объект HSM, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7b26b-127">Managed HSM object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: RemoveManagedHsmByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7b26b-128">-Name</span></span>
<span data-ttu-id="7b26b-129">Имя управляемой службы HSM, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="7b26b-129">Specifies the name of the managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b26b-130">-PassThru</span></span>
<span data-ttu-id="7b26b-131">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b26b-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="7b26b-132">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="7b26b-132">If this switch is specified, it returns true if successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b26b-133">-ResourceGroupName</span></span>
<span data-ttu-id="7b26b-134">Имя группы ресурсов для службы управления HSM Azure, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="7b26b-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b26b-135">-ResourceId</span></span>
<span data-ttu-id="7b26b-136">ManagedHsm Resource Id.</span><span class="sxs-lookup"><span data-stu-id="7b26b-136">ManagedHsm Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveManagedHsmByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b26b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b26b-137">-Confirm</span></span>
<span data-ttu-id="7b26b-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="7b26b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b26b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b26b-139">-WhatIf</span></span>
<span data-ttu-id="7b26b-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b26b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b26b-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7b26b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b26b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b26b-142">CommonParameters</span></span>
<span data-ttu-id="7b26b-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b26b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b26b-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b26b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b26b-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b26b-145">INPUTS</span></span>

### <span data-ttu-id="7b26b-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7b26b-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="7b26b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="7b26b-147">System.String</span></span>

## <span data-ttu-id="7b26b-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b26b-148">OUTPUTS</span></span>

### <span data-ttu-id="7b26b-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b26b-149">System.Boolean</span></span>

## <span data-ttu-id="7b26b-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b26b-150">NOTES</span></span>

## <span data-ttu-id="7b26b-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b26b-151">RELATED LINKS</span></span>

[<span data-ttu-id="7b26b-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7b26b-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7b26b-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7b26b-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="7b26b-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="7b26b-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)