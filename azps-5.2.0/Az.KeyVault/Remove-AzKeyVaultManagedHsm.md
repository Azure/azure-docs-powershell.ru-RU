---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 82521bd7d0ff4f34f68029cdb7faacdd198f2b02
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394884"
---
# <span data-ttu-id="6475c-101">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6475c-101">Remove-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="6475c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6475c-102">SYNOPSIS</span></span>
<span data-ttu-id="6475c-103">Удаляет управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="6475c-103">Deletes a managed HSM.</span></span>

## <span data-ttu-id="6475c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6475c-104">SYNTAX</span></span>

### <span data-ttu-id="6475c-105">RemoveManagedHsmByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6475c-105">RemoveManagedHsmByName (Default)</span></span>
```
Remove-AzKeyVaultManagedHsm [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6475c-106">RemoveManagedHsmByInputObject</span><span class="sxs-lookup"><span data-stu-id="6475c-106">RemoveManagedHsmByInputObject</span></span>
```
Remove-AzKeyVaultManagedHsm [-InputObject] <PSManagedHsm> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6475c-107">RemoveManagedHsmByResourceId</span><span class="sxs-lookup"><span data-stu-id="6475c-107">RemoveManagedHsmByResourceId</span></span>
```
Remove-AzKeyVaultManagedHsm [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6475c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6475c-108">DESCRIPTION</span></span>
<span data-ttu-id="6475c-109">**Cmdlet Remove-AzKeyVaultManagedHsm** удаляет указанный управляемый HSM.</span><span class="sxs-lookup"><span data-stu-id="6475c-109">The **Remove-AzKeyVaultManagedHsm** cmdlet deletes the specified managed HSM.</span></span>
<span data-ttu-id="6475c-110">При этом также удаляются все ключи, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="6475c-110">It also deletes all keys contained in that instance.</span></span>
<span data-ttu-id="6475c-111">Обратите внимание, что несмотря на то, что для этого cmdlet не требуется указывать группу ресурсов, это необходимо для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="6475c-111">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="6475c-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6475c-112">EXAMPLES</span></span>

### <span data-ttu-id="6475c-113">Пример 1. Удаление управляемой HSM</span><span class="sxs-lookup"><span data-stu-id="6475c-113">Example 1: Remove a managed HSM</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -Force

True
```

<span data-ttu-id="6475c-114">Эта команда удаляет управляемый хэштег myhsm из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6475c-114">This command removes the managed hsm named myhsm from your current subscription.</span></span>

### <span data-ttu-id="6475c-115">Пример 2. Удаление управляемого hsm из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6475c-115">Example 2: Remove a managed hsm from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVaultManagedHsm -HsmName 'myhsm' -ResourceGroupName "myrg1" -PassThru

True
```

<span data-ttu-id="6475c-116">Эта команда удаляет управляемый мигм с именем myhsm из группы ресурсов с именем myrg1.</span><span class="sxs-lookup"><span data-stu-id="6475c-116">This command removes the managed hsm named myhsm from the resource group named myrg1.</span></span>
<span data-ttu-id="6475c-117">Если имя группы ресурсов не указано, выполняется поиск управляемой HSM-службы, которая будет удалена из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="6475c-117">If you do not specify the resource group name, the cmdlet searches for the named managed HSM to delete in your current subscription.</span></span>

## <span data-ttu-id="6475c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6475c-118">PARAMETERS</span></span>

### <span data-ttu-id="6475c-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6475c-119">-AsJob</span></span>
<span data-ttu-id="6475c-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6475c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6475c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6475c-121">-DefaultProfile</span></span>
<span data-ttu-id="6475c-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6475c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6475c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="6475c-123">-Force</span></span>
<span data-ttu-id="6475c-124">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="6475c-124">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="6475c-125">По умолчанию этот cmdlet запросит подтверждение удаления управляемой HSM-темы.</span><span class="sxs-lookup"><span data-stu-id="6475c-125">By default, this cmdlet prompts you to confirm that you want to delete the managed HSM.</span></span>

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

### <span data-ttu-id="6475c-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6475c-126">-InputObject</span></span>
<span data-ttu-id="6475c-127">Управляемый объект HSM, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="6475c-127">Managed HSM object to be deleted.</span></span>

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

### <span data-ttu-id="6475c-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6475c-128">-Name</span></span>
<span data-ttu-id="6475c-129">Указывает имя управляемой службы HSM, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="6475c-129">Specifies the name of the managed HSM to remove.</span></span>

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

### <span data-ttu-id="6475c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6475c-130">-PassThru</span></span>
<span data-ttu-id="6475c-131">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6475c-131">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6475c-132">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="6475c-132">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6475c-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6475c-133">-ResourceGroupName</span></span>
<span data-ttu-id="6475c-134">Имя группы ресурсов для службы управления HSM Azure, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="6475c-134">Specifies the name of resource group for Azure managed HSM to remove.</span></span>

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

### <span data-ttu-id="6475c-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6475c-135">-ResourceId</span></span>
<span data-ttu-id="6475c-136">ManagedHsm Resource Id.</span><span class="sxs-lookup"><span data-stu-id="6475c-136">ManagedHsm Resource Id.</span></span>

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

### <span data-ttu-id="6475c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6475c-137">-Confirm</span></span>
<span data-ttu-id="6475c-138">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6475c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6475c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6475c-139">-WhatIf</span></span>
<span data-ttu-id="6475c-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6475c-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6475c-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6475c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6475c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6475c-142">CommonParameters</span></span>
<span data-ttu-id="6475c-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6475c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6475c-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6475c-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6475c-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6475c-145">INPUTS</span></span>

### <span data-ttu-id="6475c-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6475c-146">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="6475c-147">System.String</span><span class="sxs-lookup"><span data-stu-id="6475c-147">System.String</span></span>

## <span data-ttu-id="6475c-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6475c-148">OUTPUTS</span></span>

### <span data-ttu-id="6475c-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6475c-149">System.Boolean</span></span>

## <span data-ttu-id="6475c-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6475c-150">NOTES</span></span>

## <span data-ttu-id="6475c-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6475c-151">RELATED LINKS</span></span>

[<span data-ttu-id="6475c-152">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6475c-152">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="6475c-153">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6475c-153">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="6475c-154">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="6475c-154">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)