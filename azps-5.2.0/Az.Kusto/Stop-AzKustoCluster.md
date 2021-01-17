---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/stop-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Stop-AzKustoCluster.md
ms.openlocfilehash: 1dd67a5a3557ba38267f570c77b5117466e4260b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405060"
---
# <span data-ttu-id="1ec9e-101">Stop-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="1ec9e-101">Stop-AzKustoCluster</span></span>

## <span data-ttu-id="1ec9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec9e-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec9e-103">Остановка кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1ec9e-103">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="1ec9e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ec9e-104">SYNTAX</span></span>

### <span data-ttu-id="1ec9e-105">Остановка (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ec9e-105">Stop (Default)</span></span>
```
Stop-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1ec9e-106">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ec9e-106">StopViaIdentity</span></span>
```
Stop-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1ec9e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec9e-107">DESCRIPTION</span></span>
<span data-ttu-id="1ec9e-108">Остановка кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1ec9e-108">Stops a Kusto cluster.</span></span>

## <span data-ttu-id="1ec9e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec9e-109">EXAMPLES</span></span>

### <span data-ttu-id="1ec9e-110">Пример 1. Остановка кластера Кусто</span><span class="sxs-lookup"><span data-stu-id="1ec9e-110">Example 1: Stop a Kusto cluster</span></span>
```powershell
PS C:\> Stop-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster
```

<span data-ttu-id="1ec9e-111">При настройе выше команда останавливает кластер "Кусто"</span><span class="sxs-lookup"><span data-stu-id="1ec9e-111">The above command stops a Kusto cluster</span></span>

## <span data-ttu-id="1ec9e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec9e-112">PARAMETERS</span></span>

### <span data-ttu-id="1ec9e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ec9e-113">-AsJob</span></span>
<span data-ttu-id="1ec9e-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1ec9e-114">Run the command as a job</span></span>

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

### <span data-ttu-id="1ec9e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec9e-115">-DefaultProfile</span></span>
<span data-ttu-id="1ec9e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec9e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ec9e-117">-InputObject</span></span>
<span data-ttu-id="1ec9e-118">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1ec9e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="1ec9e-119">-Name</span></span>
<span data-ttu-id="1ec9e-120">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1ec9e-120">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1ec9e-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ec9e-121">-NoWait</span></span>
<span data-ttu-id="1ec9e-122">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1ec9e-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1ec9e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ec9e-123">-PassThru</span></span>
<span data-ttu-id="1ec9e-124">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1ec9e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ec9e-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ec9e-126">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1ec9e-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ec9e-127">-SubscriptionId</span></span>
<span data-ttu-id="1ec9e-128">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ec9e-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1ec9e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ec9e-130">-Confirm</span></span>
<span data-ttu-id="1ec9e-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ec9e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ec9e-132">-WhatIf</span></span>
<span data-ttu-id="1ec9e-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ec9e-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ec9e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec9e-135">CommonParameters</span></span>
<span data-ttu-id="1ec9e-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec9e-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1ec9e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec9e-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec9e-138">INPUTS</span></span>

### <span data-ttu-id="1ec9e-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1ec9e-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1ec9e-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec9e-140">OUTPUTS</span></span>

### <span data-ttu-id="1ec9e-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ec9e-141">System.Boolean</span></span>

## <span data-ttu-id="1ec9e-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ec9e-142">NOTES</span></span>

<span data-ttu-id="1ec9e-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1ec9e-143">ALIASES</span></span>

<span data-ttu-id="1ec9e-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1ec9e-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1ec9e-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ec9e-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1ec9e-147">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1ec9e-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ec9e-148">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1ec9e-149">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1ec9e-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1ec9e-150">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1ec9e-151">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1ec9e-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1ec9e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ec9e-153">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1ec9e-154">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="1ec9e-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1ec9e-155">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1ec9e-156">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1ec9e-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1ec9e-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1ec9e-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec9e-158">RELATED LINKS</span></span>

