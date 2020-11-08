---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 5a03df969421ea87d907efb5fe23027acfde0834
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065683"
---
# <span data-ttu-id="920fc-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="920fc-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="920fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="920fc-102">SYNOPSIS</span></span>
<span data-ttu-id="920fc-103">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="920fc-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="920fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="920fc-104">SYNTAX</span></span>

### <span data-ttu-id="920fc-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="920fc-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="920fc-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="920fc-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="920fc-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="920fc-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="920fc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="920fc-108">DESCRIPTION</span></span>
<span data-ttu-id="920fc-109">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="920fc-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="920fc-110">Настройка туннеля SSH осуществляется с помощью задания PowerShell Kubectl-Tunnel и может быть обнаружено при запуске `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="920fc-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="920fc-111">Туннель должен быть доступен через [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="920fc-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="920fc-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="920fc-112">EXAMPLES</span></span>

### <span data-ttu-id="920fc-113">Запуск туннеля SSH и открытие браузера на панели мониторинга Kubernetes</span><span class="sxs-lookup"><span data-stu-id="920fc-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="920fc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="920fc-114">PARAMETERS</span></span>

### <span data-ttu-id="920fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920fc-115">-DefaultProfile</span></span>
<span data-ttu-id="920fc-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="920fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="920fc-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="920fc-117">-DisableBrowser</span></span>
<span data-ttu-id="920fc-118">Не открывать браузер после установки порта kubectl, пересылаемого по экрану.</span><span class="sxs-lookup"><span data-stu-id="920fc-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="920fc-119">-ID</span><span class="sxs-lookup"><span data-stu-id="920fc-119">-Id</span></span>
<span data-ttu-id="920fc-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="920fc-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="920fc-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="920fc-121">-InputObject</span></span>
<span data-ttu-id="920fc-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="920fc-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="920fc-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="920fc-123">-Name</span></span>
<span data-ttu-id="920fc-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="920fc-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="920fc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="920fc-125">-PassThru</span></span>
<span data-ttu-id="920fc-126">Командлет возвращает KubeTunnelJob, если он передан.</span><span class="sxs-lookup"><span data-stu-id="920fc-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="920fc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920fc-127">-ResourceGroupName</span></span>
<span data-ttu-id="920fc-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="920fc-128">Resource group name</span></span>

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

### <span data-ttu-id="920fc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920fc-129">CommonParameters</span></span>
<span data-ttu-id="920fc-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="920fc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920fc-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920fc-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920fc-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="920fc-132">INPUTS</span></span>

### <span data-ttu-id="920fc-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="920fc-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="920fc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="920fc-134">System.String</span></span>

## <span data-ttu-id="920fc-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="920fc-135">OUTPUTS</span></span>

### <span data-ttu-id="920fc-136">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="920fc-136">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="920fc-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="920fc-137">NOTES</span></span>

## <span data-ttu-id="920fc-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="920fc-138">RELATED LINKS</span></span>
