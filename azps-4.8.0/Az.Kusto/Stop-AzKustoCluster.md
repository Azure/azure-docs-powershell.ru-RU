---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078207"
---
# <span data-ttu-id="4e9b3-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="4e9b3-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="4e9b3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9b3-103">Останавливает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="4e9b3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e9b3-104">SYNTAX</span></span>

### <span data-ttu-id="4e9b3-105">Остановить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e9b3-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e9b3-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e9b3-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e9b3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-107">DESCRIPTION</span></span>
<span data-ttu-id="4e9b3-108">Останавливает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="4e9b3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-109">EXAMPLES</span></span>

### <span data-ttu-id="4e9b3-110">Пример 1: остановка кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="4e9b3-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="4e9b3-111">Указанная выше команда останавливает кластер Kusto</span><span class="sxs-lookup"><span data-stu-id="4e9b3-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="4e9b3-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-112">PARAMETERS</span></span>

### <span data-ttu-id="4e9b3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e9b3-113">-AsJob</span></span>
<span data-ttu-id="4e9b3-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4e9b3-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4e9b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e9b3-115">-DefaultProfile</span></span>
<span data-ttu-id="4e9b3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e9b3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e9b3-117">-InputObject</span></span>
<span data-ttu-id="4e9b3-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e9b3-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e9b3-119">-Name</span></span>
<span data-ttu-id="4e9b3-120">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9b3-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="4e9b3-121">-NoWait</span></span>
<span data-ttu-id="4e9b3-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="4e9b3-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e9b3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4e9b3-123">-PassThru</span></span>
<span data-ttu-id="4e9b3-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4e9b3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9b3-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e9b3-126">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9b3-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e9b3-127">-SubscriptionId</span></span>
<span data-ttu-id="4e9b3-128">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e9b3-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e9b3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e9b3-130">-Confirm</span></span>
<span data-ttu-id="4e9b3-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e9b3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e9b3-132">-WhatIf</span></span>
<span data-ttu-id="4e9b3-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e9b3-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e9b3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9b3-135">CommonParameters</span></span>
<span data-ttu-id="4e9b3-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9b3-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4e9b3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9b3-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e9b3-138">INPUTS</span></span>

### <span data-ttu-id="4e9b3-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4e9b3-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4e9b3-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-140">OUTPUTS</span></span>

### <span data-ttu-id="4e9b3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4e9b3-141">System.Boolean</span></span>

## <span data-ttu-id="4e9b3-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e9b3-142">NOTES</span></span>

<span data-ttu-id="4e9b3-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-143">ALIASES</span></span>

<span data-ttu-id="4e9b3-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e9b3-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e9b3-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e9b3-147">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4e9b3-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e9b3-148">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4e9b3-149">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4e9b3-150">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4e9b3-151">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4e9b3-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4e9b3-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e9b3-153">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4e9b3-154">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4e9b3-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4e9b3-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e9b3-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4e9b3-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4e9b3-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e9b3-158">RELATED LINKS</span></span>

