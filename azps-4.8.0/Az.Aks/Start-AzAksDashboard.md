---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/start-azaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Start-AzAksDashboard.md
ms.openlocfilehash: 91e4ec27298fa3fead3041e43f988b96ecf64046
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079293"
---
# <span data-ttu-id="76f09-101">Start-AzAksDashboard</span><span class="sxs-lookup"><span data-stu-id="76f09-101">Start-AzAksDashboard</span></span>

## <span data-ttu-id="76f09-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76f09-102">SYNOPSIS</span></span>
<span data-ttu-id="76f09-103">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="76f09-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

## <span data-ttu-id="76f09-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76f09-104">SYNTAX</span></span>

### <span data-ttu-id="76f09-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76f09-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-ListenPort <Int32>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f09-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f09-106">InputObjectParameterSet</span></span>
```
Start-AzAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76f09-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76f09-107">IdParameterSet</span></span>
```
Start-AzAksDashboard [-Id] <String> [-DisableBrowser] [-ListenPort <Int32>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="76f09-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76f09-108">DESCRIPTION</span></span>
<span data-ttu-id="76f09-109">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="76f09-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="76f09-110">Настройка туннеля SSH осуществляется с помощью задания PowerShell Kubectl-Tunnel и может быть обнаружено при запуске `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="76f09-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="76f09-111">Туннель должен быть доступен через [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="76f09-111">The tunnel should be accessible via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="76f09-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76f09-112">EXAMPLES</span></span>

### <span data-ttu-id="76f09-113">Запуск туннеля SSH и открытие браузера на панели мониторинга Kubernetes</span><span class="sxs-lookup"><span data-stu-id="76f09-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="76f09-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76f09-114">PARAMETERS</span></span>

### <span data-ttu-id="76f09-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f09-115">-DefaultProfile</span></span>
<span data-ttu-id="76f09-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76f09-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76f09-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="76f09-117">-DisableBrowser</span></span>
<span data-ttu-id="76f09-118">Не открывать браузер после установки порта kubectl, пересылаемого по экрану.</span><span class="sxs-lookup"><span data-stu-id="76f09-118">Do not pop open a browser after establishing the kubectl port-forward.</span></span>

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

### <span data-ttu-id="76f09-119">-ID</span><span class="sxs-lookup"><span data-stu-id="76f09-119">-Id</span></span>
<span data-ttu-id="76f09-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="76f09-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="76f09-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76f09-121">-InputObject</span></span>
<span data-ttu-id="76f09-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="76f09-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="76f09-123">-ListenPort</span><span class="sxs-lookup"><span data-stu-id="76f09-123">-ListenPort</span></span>
<span data-ttu-id="76f09-124">Прослушивающий порт для панели мониторинга.</span><span class="sxs-lookup"><span data-stu-id="76f09-124">The listening port for the dashboard.</span></span> <span data-ttu-id="76f09-125">Значение по умолчанию — 8003.</span><span class="sxs-lookup"><span data-stu-id="76f09-125">Default value is 8003.</span></span>

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

### <span data-ttu-id="76f09-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76f09-126">-Name</span></span>
<span data-ttu-id="76f09-127">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="76f09-127">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="76f09-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76f09-128">-PassThru</span></span>
<span data-ttu-id="76f09-129">Командлет возвращает KubeTunnelJob, если он передан.</span><span class="sxs-lookup"><span data-stu-id="76f09-129">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="76f09-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f09-130">-ResourceGroupName</span></span>
<span data-ttu-id="76f09-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="76f09-131">Resource group name</span></span>

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

### <span data-ttu-id="76f09-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f09-132">CommonParameters</span></span>
<span data-ttu-id="76f09-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76f09-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f09-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76f09-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f09-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76f09-135">INPUTS</span></span>

### <span data-ttu-id="76f09-136">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="76f09-136">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="76f09-137">System. String</span><span class="sxs-lookup"><span data-stu-id="76f09-137">System.String</span></span>

## <span data-ttu-id="76f09-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76f09-138">OUTPUTS</span></span>

### <span data-ttu-id="76f09-139">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="76f09-139">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="76f09-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="76f09-140">NOTES</span></span>

## <span data-ttu-id="76f09-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76f09-141">RELATED LINKS</span></span>
