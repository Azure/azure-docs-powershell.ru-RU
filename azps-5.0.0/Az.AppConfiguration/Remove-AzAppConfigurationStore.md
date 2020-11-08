---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246445"
---
# <span data-ttu-id="346d7-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="346d7-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="346d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="346d7-102">SYNOPSIS</span></span>
<span data-ttu-id="346d7-103">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="346d7-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="346d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="346d7-104">SYNTAX</span></span>

### <span data-ttu-id="346d7-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="346d7-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="346d7-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="346d7-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="346d7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="346d7-107">DESCRIPTION</span></span>
<span data-ttu-id="346d7-108">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="346d7-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="346d7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="346d7-109">EXAMPLES</span></span>

### <span data-ttu-id="346d7-110">Пример 1: Удаление хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="346d7-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="346d7-111">Эта команда удаляет хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="346d7-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="346d7-112">Пример 2: Удаление хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="346d7-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="346d7-113">Эта команда удаляет хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="346d7-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="346d7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="346d7-114">PARAMETERS</span></span>

### <span data-ttu-id="346d7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="346d7-115">-AsJob</span></span>
<span data-ttu-id="346d7-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="346d7-116">Run the command as a job</span></span>

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

### <span data-ttu-id="346d7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="346d7-117">-DefaultProfile</span></span>
<span data-ttu-id="346d7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="346d7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="346d7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="346d7-119">-InputObject</span></span>
<span data-ttu-id="346d7-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="346d7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="346d7-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="346d7-121">-Name</span></span>
<span data-ttu-id="346d7-122">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="346d7-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="346d7-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="346d7-123">-NoWait</span></span>
<span data-ttu-id="346d7-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="346d7-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="346d7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="346d7-125">-PassThru</span></span>
<span data-ttu-id="346d7-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="346d7-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="346d7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="346d7-127">-ResourceGroupName</span></span>
<span data-ttu-id="346d7-128">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="346d7-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="346d7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="346d7-129">-SubscriptionId</span></span>
<span data-ttu-id="346d7-130">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="346d7-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="346d7-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="346d7-131">-Confirm</span></span>
<span data-ttu-id="346d7-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="346d7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="346d7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="346d7-133">-WhatIf</span></span>
<span data-ttu-id="346d7-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="346d7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="346d7-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="346d7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="346d7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="346d7-136">CommonParameters</span></span>
<span data-ttu-id="346d7-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="346d7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="346d7-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="346d7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="346d7-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="346d7-139">INPUTS</span></span>

### <span data-ttu-id="346d7-140">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="346d7-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="346d7-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="346d7-141">OUTPUTS</span></span>

### <span data-ttu-id="346d7-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="346d7-142">System.Boolean</span></span>

## <span data-ttu-id="346d7-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="346d7-143">NOTES</span></span>

<span data-ttu-id="346d7-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="346d7-144">ALIASES</span></span>

<span data-ttu-id="346d7-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="346d7-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="346d7-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="346d7-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="346d7-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="346d7-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="346d7-148">INPUTOBJECT <IAppConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="346d7-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="346d7-149">`[ConfigStoreName <String>]`: Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="346d7-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="346d7-150">`[GroupName <String>]`: Имя группы ресурсов частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="346d7-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="346d7-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="346d7-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="346d7-152">`[PrivateEndpointConnectionName <String>]`: Имя частного подключения конечной точки</span><span class="sxs-lookup"><span data-stu-id="346d7-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="346d7-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="346d7-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="346d7-154">`[SubscriptionId <String>]`: Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="346d7-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="346d7-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="346d7-155">RELATED LINKS</span></span>

