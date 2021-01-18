---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506979"
---
# <span data-ttu-id="268fd-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="268fd-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="268fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="268fd-102">SYNOPSIS</span></span>
<span data-ttu-id="268fd-103">Создайте ASH-туннель Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="268fd-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="268fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="268fd-104">SYNTAX</span></span>

### <span data-ttu-id="268fd-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="268fd-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268fd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="268fd-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="268fd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="268fd-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="268fd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="268fd-108">DESCRIPTION</span></span>
<span data-ttu-id="268fd-109">Создайте ASH-туннель Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="268fd-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="268fd-110">SSH-туннель настроен в задание PowerShell Kubectl-Tunnel и его можно найти с помощью `Get-Job` запуска.</span><span class="sxs-lookup"><span data-stu-id="268fd-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="268fd-111">Туннель должен быть доступен через [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="268fd-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="268fd-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="268fd-112">EXAMPLES</span></span>

### <span data-ttu-id="268fd-113">Запуск туннель SSH и открытие браузера на панели мониторинга Kubernetes</span><span class="sxs-lookup"><span data-stu-id="268fd-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="268fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="268fd-114">PARAMETERS</span></span>

### <span data-ttu-id="268fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="268fd-115">-DefaultProfile</span></span>
<span data-ttu-id="268fd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="268fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="268fd-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="268fd-117">-DisableBrowser</span></span>
<span data-ttu-id="268fd-118">Не открывай браузер после создания перенапрямленного порта kubectl.</span><span class="sxs-lookup"><span data-stu-id="268fd-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="268fd-119">-Id</span><span class="sxs-lookup"><span data-stu-id="268fd-119">-Id</span></span>
<span data-ttu-id="268fd-120">ИД кластера "Управляемые кубберсети"</span><span class="sxs-lookup"><span data-stu-id="268fd-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="268fd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="268fd-121">-InputObject</span></span>
<span data-ttu-id="268fd-122">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="268fd-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="268fd-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="268fd-123">-ListenPort</span></span>
<span data-ttu-id="268fd-124">Порт прослушивания панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="268fd-124">The listening port for the dashboard.</span></span> <span data-ttu-id="268fd-125">Значение по умолчанию — 8003.</span><span class="sxs-lookup"><span data-stu-id="268fd-125">Default value is 8003.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268fd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="268fd-126">-Name</span></span>
<span data-ttu-id="268fd-127">Название кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="268fd-127">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268fd-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="268fd-128">-PassThru</span></span>
<span data-ttu-id="268fd-129">Если он прошел, cmdlet возвращает KubeTunnelJob.</span><span class="sxs-lookup"><span data-stu-id="268fd-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="268fd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="268fd-130">-ResourceGroupName</span></span>
<span data-ttu-id="268fd-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="268fd-131">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="268fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="268fd-132">CommonParameters</span></span>
<span data-ttu-id="268fd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="268fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="268fd-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="268fd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="268fd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="268fd-135">INPUTS</span></span>

### <span data-ttu-id="268fd-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="268fd-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="268fd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="268fd-137">System.String</span></span>

## <span data-ttu-id="268fd-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="268fd-138">OUTPUTS</span></span>

### <span data-ttu-id="268fd-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="268fd-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="268fd-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="268fd-140">NOTES</span></span>

## <span data-ttu-id="268fd-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="268fd-141">RELATED LINKS</span></span>
