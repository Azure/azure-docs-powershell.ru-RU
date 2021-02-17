---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 7A929BA8-02D9-4BBE-AFF3-B8781F8DDAD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVault.md
ms.openlocfilehash: 69a1155b99d054699c41cc0b26cd78ef4445f931
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234065"
---
# <span data-ttu-id="1f27b-101">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-101">Remove-AzKeyVault</span></span>

## <span data-ttu-id="1f27b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f27b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f27b-103">Удаляет хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1f27b-103">Deletes a key vault.</span></span>

## <span data-ttu-id="1f27b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1f27b-104">SYNTAX</span></span>

### <span data-ttu-id="1f27b-105">ByAvailableVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1f27b-105">ByAvailableVault (Default)</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>] [[-Location] <String>] [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f27b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-106">ByDeletedVault</span></span>
```
Remove-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f27b-107">InputObjectByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-107">InputObjectByAvailableVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f27b-108">InputObjectByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-108">InputObjectByDeletedVault</span></span>
```
Remove-AzKeyVault [-InputObject] <PSKeyVault> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f27b-109">ResourceIdByAvailableVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-109">ResourceIdByAvailableVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [[-Location] <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f27b-110">ResourceIdByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-110">ResourceIdByDeletedVault</span></span>
```
Remove-AzKeyVault [-ResourceId] <String> [-Location] <String> [-InRemovedState] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f27b-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f27b-111">DESCRIPTION</span></span>
<span data-ttu-id="1f27b-112">При **нажатии на клавишу Remove-AzKeyVault** удаляется указанный ключ.</span><span class="sxs-lookup"><span data-stu-id="1f27b-112">The **Remove-AzKeyVault** cmdlet deletes the specified key vault.</span></span>
<span data-ttu-id="1f27b-113">Здесь также удаляются все ключи и секреты, содержащиеся в этом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="1f27b-113">It also deletes all keys and secrets contained in that instance.</span></span>
<span data-ttu-id="1f27b-114">Обратите внимание, что несмотря на то, что для этого cmdlet не требуется указывать группу ресурсов, это необходимо для улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="1f27b-114">Note that although specifying the resource group is optional for this cmdlet, you should so for better performance.</span></span>

## <span data-ttu-id="1f27b-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1f27b-115">EXAMPLES</span></span>

### <span data-ttu-id="1f27b-116">Пример 1. Удаление сейфа ключа</span><span class="sxs-lookup"><span data-stu-id="1f27b-116">Example 1: Remove a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVault -VaultName "Contoso03Vault" -PassThru

True
```

<span data-ttu-id="1f27b-117">Эта команда удаляет из текущей подписки хранилище ключей Contoso03Vault.</span><span class="sxs-lookup"><span data-stu-id="1f27b-117">This command removes the key vault named Contoso03Vault from your current subscription.</span></span>

### <span data-ttu-id="1f27b-118">Пример 2. Удаление сейфа ключа из указанной группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1f27b-118">Example 2: Remove a key vault from a specified resource group</span></span>
```powershell
PS C:\> Remove-AzKeyVault -Name "Contoso03Vault" -ResourceGroupName "Group14" -PassThru

True
```

<span data-ttu-id="1f27b-119">Эта команда удаляет хранилище ключей Contoso03Vault из именоваемой группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f27b-119">This command removes the key vault named Contoso03Vault from the named resource group.</span></span>
<span data-ttu-id="1f27b-120">Если имя группы ресурсов не указано, выполняется поиск именоваемого хранилища ключей для удаления в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1f27b-120">If you do not specify the resource group name, the cmdlet searches for the named key vault to delete in your current subscription.</span></span>

### <span data-ttu-id="1f27b-121">Пример 3. Удаление управляемого hsm</span><span class="sxs-lookup"><span data-stu-id="1f27b-121">Example 3: Remove a managed hsm</span></span>
```powershell
PS C:\>  Remove-AzKeyVault -Name "testManagedHsm" -Hsm -PassThru

True
```

<span data-ttu-id="1f27b-122">Эта команда удаляет управляемый hsm testManagedHsm из текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1f27b-122">This command removes the managed hsm named testManagedHsm from your current subscription.</span></span>

## <span data-ttu-id="1f27b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f27b-123">PARAMETERS</span></span>

### <span data-ttu-id="1f27b-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f27b-124">-AsJob</span></span>
<span data-ttu-id="1f27b-125">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1f27b-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f27b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f27b-126">-DefaultProfile</span></span>
<span data-ttu-id="1f27b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1f27b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f27b-128">-Force</span><span class="sxs-lookup"><span data-stu-id="1f27b-128">-Force</span></span>
<span data-ttu-id="1f27b-129">Указывает на то, что при этом не будет предложено подтвердить запрос.</span><span class="sxs-lookup"><span data-stu-id="1f27b-129">Indicates that the cmdlet does not prompt you for confirmation.</span></span>
<span data-ttu-id="1f27b-130">По умолчанию этот cmdlet запросит подтверждение удаления хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1f27b-130">By default, this cmdlet prompts you to confirm that you want to delete the key vault.</span></span>

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

### <span data-ttu-id="1f27b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f27b-131">-InputObject</span></span>
<span data-ttu-id="1f27b-132">Объект key Vault, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1f27b-132">Key Vault object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByAvailableVault, InputObjectByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-133">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="1f27b-133">-InRemovedState</span></span>
<span data-ttu-id="1f27b-134">Окончательное удаление ранее удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="1f27b-134">Remove the previously deleted vault permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, InputObjectByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-135">-Location</span><span class="sxs-lookup"><span data-stu-id="1f27b-135">-Location</span></span>
<span data-ttu-id="1f27b-136">Расположение удаленного сейфа.</span><span class="sxs-lookup"><span data-stu-id="1f27b-136">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ResourceIdByAvailableVault
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f27b-137">-PassThru</span></span>
<span data-ttu-id="1f27b-138">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1f27b-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="1f27b-139">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="1f27b-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1f27b-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f27b-140">-ResourceGroupName</span></span>
<span data-ttu-id="1f27b-141">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f27b-141">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f27b-142">-ResourceId</span></span>
<span data-ttu-id="1f27b-143">ИД ресурса KeyVault.</span><span class="sxs-lookup"><span data-stu-id="1f27b-143">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableVault, ResourceIdByDeletedVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1f27b-144">-VaultName</span></span>
<span data-ttu-id="1f27b-145">Указывает имя сейфа ключа, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1f27b-145">Specifies the name of the key vault to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableVault, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f27b-146">-Confirm</span></span>
<span data-ttu-id="1f27b-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1f27b-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f27b-148">-WhatIf</span></span>
<span data-ttu-id="1f27b-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f27b-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f27b-150">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f27b-150">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f27b-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1f27b-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f27b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f27b-152">CommonParameters</span></span>
<span data-ttu-id="1f27b-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f27b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f27b-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f27b-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f27b-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f27b-155">INPUTS</span></span>

### <span data-ttu-id="1f27b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1f27b-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1f27b-157">System.String</span></span>

## <span data-ttu-id="1f27b-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1f27b-158">OUTPUTS</span></span>

### <span data-ttu-id="1f27b-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1f27b-159">System.Boolean</span></span>

## <span data-ttu-id="1f27b-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1f27b-160">NOTES</span></span>

## <span data-ttu-id="1f27b-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f27b-161">RELATED LINKS</span></span>

[<span data-ttu-id="1f27b-162">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-162">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="1f27b-163">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="1f27b-163">New-AzKeyVault</span></span>](./New-AzKeyVault.md)
