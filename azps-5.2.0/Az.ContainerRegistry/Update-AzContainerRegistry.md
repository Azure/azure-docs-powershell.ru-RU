---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 22dfee058a26163206c973f664615a4f29ae61de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391991"
---
# <span data-ttu-id="9215b-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9215b-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="9215b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9215b-102">SYNOPSIS</span></span>
<span data-ttu-id="9215b-103">Обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="9215b-103">Updates a container registry.</span></span>

## <span data-ttu-id="9215b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9215b-104">SYNTAX</span></span>

### <span data-ttu-id="9215b-105">NameResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9215b-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9215b-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9215b-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9215b-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9215b-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9215b-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9215b-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9215b-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9215b-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9215b-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9215b-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Sku <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9215b-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9215b-111">DESCRIPTION</span></span>
<span data-ttu-id="9215b-112">Новый Update-AzContainerRegistry обновляет реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="9215b-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="9215b-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9215b-113">EXAMPLES</span></span>

### <span data-ttu-id="9215b-114">Пример 1. Enable admin user for a specified container registry</span><span class="sxs-lookup"><span data-stu-id="9215b-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="9215b-115">Эта команда позволяет администратору использовать указанный реестр контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9215b-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="9215b-116">Пример 2. Настройка учетной записи хранения, используемой указанным реестром контейнеров</span><span class="sxs-lookup"><span data-stu-id="9215b-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="9215b-117">Эта команда задает для указанного реестра контейнера существующую учетную запись хранения \` mystorageaccount \` в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="9215b-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="9215b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9215b-118">PARAMETERS</span></span>

### <span data-ttu-id="9215b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9215b-119">-DefaultProfile</span></span>
<span data-ttu-id="9215b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9215b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9215b-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9215b-121">-DisableAdminUser</span></span>
<span data-ttu-id="9215b-122">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9215b-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="9215b-123">-EnableAdminUser</span></span>
<span data-ttu-id="9215b-124">Включить пользователя администратора для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9215b-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9215b-125">-Name</span></span>
<span data-ttu-id="9215b-126">Имя реестра контейнера.</span><span class="sxs-lookup"><span data-stu-id="9215b-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-127">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="9215b-127">-NetworkRuleSet</span></span>
<span data-ttu-id="9215b-128">Сетевое правило для реестра контейнеров.</span><span class="sxs-lookup"><span data-stu-id="9215b-128">The network rule set for a container registry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9215b-129">-ResourceGroupName</span></span>
<span data-ttu-id="9215b-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9215b-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9215b-131">-ResourceId</span></span>
<span data-ttu-id="9215b-132">ИД контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="9215b-132">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="9215b-133">-Sku</span></span>
<span data-ttu-id="9215b-134">Container Registry SKU.</span><span class="sxs-lookup"><span data-stu-id="9215b-134">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9215b-135">-StorageAccountName</span></span>
<span data-ttu-id="9215b-136">Имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9215b-136">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="9215b-137">-Tag</span></span>
<span data-ttu-id="9215b-138">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="9215b-138">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="9215b-139">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9215b-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9215b-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9215b-140">-Confirm</span></span>
<span data-ttu-id="9215b-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9215b-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9215b-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9215b-142">-WhatIf</span></span>
<span data-ttu-id="9215b-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9215b-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9215b-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9215b-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9215b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9215b-145">CommonParameters</span></span>
<span data-ttu-id="9215b-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9215b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9215b-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9215b-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9215b-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9215b-148">INPUTS</span></span>

### <span data-ttu-id="9215b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9215b-149">System.String</span></span>

## <span data-ttu-id="9215b-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9215b-150">OUTPUTS</span></span>

### <span data-ttu-id="9215b-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9215b-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="9215b-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9215b-152">NOTES</span></span>

## <span data-ttu-id="9215b-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9215b-153">RELATED LINKS</span></span>

[<span data-ttu-id="9215b-154">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9215b-154">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="9215b-155">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9215b-155">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="9215b-156">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="9215b-156">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

