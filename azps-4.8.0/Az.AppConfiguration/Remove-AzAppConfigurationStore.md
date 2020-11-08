---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/remove-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Remove-AzAppConfigurationStore.md
ms.openlocfilehash: b0939a4baa498532a3b519875183e6d1d12945a7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243729"
---
# <span data-ttu-id="0fa84-101">Remove-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="0fa84-101">Remove-AzAppConfigurationStore</span></span>

## <span data-ttu-id="0fa84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fa84-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa84-103">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0fa84-103">Deletes a configuration store.</span></span>

## <span data-ttu-id="0fa84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fa84-104">SYNTAX</span></span>

### <span data-ttu-id="0fa84-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fa84-105">Delete (Default)</span></span>
```
Remove-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0fa84-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fa84-106">DeleteViaIdentity</span></span>
```
Remove-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fa84-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fa84-107">DESCRIPTION</span></span>
<span data-ttu-id="0fa84-108">Удаляет хранилище конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0fa84-108">Deletes a configuration store.</span></span>

## <span data-ttu-id="0fa84-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fa84-109">EXAMPLES</span></span>

### <span data-ttu-id="0fa84-110">Пример 1: Удаление хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="0fa84-110">Example 1: Remove an app configuration store</span></span>
```powershell
PS C:\> Remove-AzAppConfigurationStore -Name appconfig-test03 -ResourceGroupName lucas-manual-test

```

<span data-ttu-id="0fa84-111">Эта команда удаляет хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="0fa84-111">This command removes an app configuration store.</span></span>

### <span data-ttu-id="0fa84-112">Пример 2: Удаление хранилища конфигурации приложения</span><span class="sxs-lookup"><span data-stu-id="0fa84-112">Example 2: Remove an app configuration store</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -Name appconfig-test02 -ResourceGroupName lucas-manual-test | Remove-AzAppConfigurationStore

```

<span data-ttu-id="0fa84-113">Эта команда удаляет хранилище конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="0fa84-113">This command removes an app configuration store.</span></span>

## <span data-ttu-id="0fa84-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fa84-114">PARAMETERS</span></span>

### <span data-ttu-id="0fa84-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fa84-115">-AsJob</span></span>
<span data-ttu-id="0fa84-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0fa84-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0fa84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa84-117">-DefaultProfile</span></span>
<span data-ttu-id="0fa84-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa84-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa84-119">-InputObject</span></span>
<span data-ttu-id="0fa84-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0fa84-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0fa84-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fa84-121">-Name</span></span>
<span data-ttu-id="0fa84-122">Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0fa84-122">The name of the configuration store.</span></span>

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

### <span data-ttu-id="0fa84-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="0fa84-123">-NoWait</span></span>
<span data-ttu-id="0fa84-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0fa84-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fa84-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa84-125">-PassThru</span></span>
<span data-ttu-id="0fa84-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0fa84-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fa84-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa84-127">-ResourceGroupName</span></span>
<span data-ttu-id="0fa84-128">Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fa84-128">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="0fa84-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fa84-129">-SubscriptionId</span></span>
<span data-ttu-id="0fa84-130">Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa84-130">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="0fa84-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fa84-131">-Confirm</span></span>
<span data-ttu-id="0fa84-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fa84-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa84-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa84-133">-WhatIf</span></span>
<span data-ttu-id="0fa84-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fa84-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa84-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fa84-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa84-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa84-136">CommonParameters</span></span>
<span data-ttu-id="0fa84-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fa84-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa84-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fa84-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa84-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fa84-139">INPUTS</span></span>

### <span data-ttu-id="0fa84-140">Microsoft. Azure. PowerShell. командлеты. AppConfiguration. Models. IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="0fa84-140">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="0fa84-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fa84-141">OUTPUTS</span></span>

### <span data-ttu-id="0fa84-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa84-142">System.Boolean</span></span>

## <span data-ttu-id="0fa84-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fa84-143">NOTES</span></span>

<span data-ttu-id="0fa84-144">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0fa84-144">ALIASES</span></span>

<span data-ttu-id="0fa84-145">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0fa84-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fa84-146">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0fa84-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fa84-147">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fa84-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fa84-148">INPUTOBJECT <IAppConfigurationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0fa84-148">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fa84-149">`[ConfigStoreName <String>]`: Имя хранилища конфигураций.</span><span class="sxs-lookup"><span data-stu-id="0fa84-149">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="0fa84-150">`[GroupName <String>]`: Имя группы ресурсов частной ссылки.</span><span class="sxs-lookup"><span data-stu-id="0fa84-150">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="0fa84-151">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0fa84-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fa84-152">`[PrivateEndpointConnectionName <String>]`: Имя частного подключения конечной точки</span><span class="sxs-lookup"><span data-stu-id="0fa84-152">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="0fa84-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, к которой принадлежит реестр контейнера.</span><span class="sxs-lookup"><span data-stu-id="0fa84-153">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="0fa84-154">`[SubscriptionId <String>]`: Идентификатор подписки Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa84-154">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="0fa84-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fa84-155">RELATED LINKS</span></span>

