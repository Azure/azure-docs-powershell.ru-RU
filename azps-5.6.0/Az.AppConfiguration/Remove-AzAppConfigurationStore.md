---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: 4babe23fbddbc11838cad6307117884c3bb14ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990576"
---
# <span data-ttu-id="6ff7d-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="6ff7d-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="6ff7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ff7d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff7d-103">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="6ff7d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ff7d-104">SYNTAX</span></span>

### <span data-ttu-id="6ff7d-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ff7d-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6ff7d-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ff7d-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ff7d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ff7d-107">DESCRIPTION</span></span>
<span data-ttu-id="6ff7d-108">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="6ff7d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ff7d-109">EXAMPLES</span></span>

### <span data-ttu-id="6ff7d-110">Пример 1. Удаление магазина конфигурации приложений</span><span class="sxs-lookup"><span data-stu-id="6ff7d-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="6ff7d-111">Эта команда удаляет магазин конфигурации приложений.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="6ff7d-112">Пример 2. Удаление магазина конфигурации приложений</span><span class="sxs-lookup"><span data-stu-id="6ff7d-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="6ff7d-113">Эта команда удаляет хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="6ff7d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ff7d-114">PARAMETERS</span></span>

### <span data-ttu-id="6ff7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ff7d-115">-AsJob</span></span>
<span data-ttu-id="6ff7d-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="6ff7d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6ff7d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff7d-117">-DefaultProfile</span></span>
<span data-ttu-id="6ff7d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff7d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ff7d-119">-InputObject</span></span>
<span data-ttu-id="6ff7d-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ff7d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6ff7d-121">-Name</span></span>
<span data-ttu-id="6ff7d-122">Имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-122">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff7d-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6ff7d-123">-NoWait</span></span>
<span data-ttu-id="6ff7d-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="6ff7d-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ff7d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff7d-125">-PassThru</span></span>
<span data-ttu-id="6ff7d-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6ff7d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff7d-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ff7d-128">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-128">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff7d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ff7d-129">-SubscriptionId</span></span>
<span data-ttu-id="6ff7d-130">ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-130">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ff7d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ff7d-131">-Confirm</span></span>
<span data-ttu-id="6ff7d-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff7d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff7d-133">-WhatIf</span></span>
<span data-ttu-id="6ff7d-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff7d-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff7d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff7d-136">CommonParameters</span></span>
<span data-ttu-id="6ff7d-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff7d-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ff7d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff7d-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ff7d-139">INPUTS</span></span>

### <span data-ttu-id="6ff7d-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="6ff7d-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="6ff7d-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ff7d-141">OUTPUTS</span></span>

### <span data-ttu-id="6ff7d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6ff7d-142">System.Boolean</span></span>

## <span data-ttu-id="6ff7d-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ff7d-143">NOTES</span></span>

<span data-ttu-id="6ff7d-144">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6ff7d-144">ALIASES</span></span>

<span data-ttu-id="6ff7d-145">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6ff7d-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ff7d-146">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ff7d-147">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ff7d-148">INPUTOBJECT <IAppConfigurationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6ff7d-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ff7d-149">`[ConfigStoreName <String>]`: имя магазина конфигурации.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="6ff7d-150">`[GroupName <String>]`: Имя закрытой группы ресурсов, связываемой с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="6ff7d-151">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6ff7d-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ff7d-152">`[PrivateEndpointConnectionName <String>]`: имя подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="6ff7d-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="6ff7d-153">`[ResourceGroupName <String>]`: имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="6ff7d-154">`[SubscriptionId <String>]`: ИД подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff7d-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="6ff7d-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ff7d-155">RELATED LINKS</span></span>

