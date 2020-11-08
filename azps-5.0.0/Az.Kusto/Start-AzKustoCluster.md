---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/start-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Start-AzKustoCluster.md
ms.openlocfilehash: 5258fc6685e57224b51c3be45c64191076136221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248971"
---
# <span data-ttu-id="0a29a-101">Start-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="0a29a-101">Start-AzKustoCluster</span></span>

## <span data-ttu-id="0a29a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a29a-102">SYNOPSIS</span></span>
<span data-ttu-id="0a29a-103">Запускает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-103">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="0a29a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a29a-104">SYNTAX</span></span>

### <span data-ttu-id="0a29a-105">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a29a-105">Start (Default)</span></span>
```
Start-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0a29a-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a29a-106">StartViaIdentity</span></span>
```
Start-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0a29a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a29a-107">DESCRIPTION</span></span>
<span data-ttu-id="0a29a-108">Запускает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-108">Starts a Kusto cluster.</span></span>

## <span data-ttu-id="0a29a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a29a-109">EXAMPLES</span></span>

### <span data-ttu-id="0a29a-110">Пример 1: запуск кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="0a29a-110">Example 1: Start a Kusto cluster</span></span>
```powershell
PS C:\> Start-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="0a29a-111">Вышеприведенная команда запускает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-111">The above command starts a Kusto cluster.</span></span>

## <span data-ttu-id="0a29a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a29a-112">PARAMETERS</span></span>

### <span data-ttu-id="0a29a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a29a-113">-AsJob</span></span>
<span data-ttu-id="0a29a-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0a29a-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0a29a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a29a-115">-DefaultProfile</span></span>
<span data-ttu-id="0a29a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a29a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a29a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a29a-117">-InputObject</span></span>
<span data-ttu-id="0a29a-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0a29a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a29a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a29a-119">-Name</span></span>
<span data-ttu-id="0a29a-120">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-120">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a29a-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="0a29a-121">-NoWait</span></span>
<span data-ttu-id="0a29a-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0a29a-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a29a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a29a-123">-PassThru</span></span>
<span data-ttu-id="0a29a-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0a29a-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a29a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a29a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0a29a-126">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a29a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a29a-127">-SubscriptionId</span></span>
<span data-ttu-id="0a29a-128">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a29a-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a29a-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0a29a-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a29a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a29a-130">-Confirm</span></span>
<span data-ttu-id="0a29a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a29a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a29a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a29a-132">-WhatIf</span></span>
<span data-ttu-id="0a29a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a29a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a29a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a29a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a29a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a29a-135">CommonParameters</span></span>
<span data-ttu-id="0a29a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a29a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a29a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a29a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a29a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a29a-138">INPUTS</span></span>

### <span data-ttu-id="0a29a-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0a29a-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0a29a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a29a-140">OUTPUTS</span></span>

### <span data-ttu-id="0a29a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0a29a-141">System.Boolean</span></span>

## <span data-ttu-id="0a29a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a29a-142">NOTES</span></span>

<span data-ttu-id="0a29a-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0a29a-143">ALIASES</span></span>

<span data-ttu-id="0a29a-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0a29a-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a29a-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a29a-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a29a-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a29a-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a29a-147">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0a29a-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a29a-148">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a29a-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0a29a-149">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0a29a-150">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0a29a-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0a29a-151">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0a29a-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0a29a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a29a-153">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="0a29a-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0a29a-154">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0a29a-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0a29a-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a29a-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0a29a-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a29a-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0a29a-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0a29a-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0a29a-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a29a-158">RELATED LINKS</span></span>

