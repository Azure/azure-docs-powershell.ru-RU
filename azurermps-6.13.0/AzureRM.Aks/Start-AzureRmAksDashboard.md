---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/start-azurermaksdashboard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Start-AzureRmAksDashboard.md
ms.openlocfilehash: bf9ad8306a8158d9a8087de1f299ba66a02717fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733927"
---
# <span data-ttu-id="66932-101">Start-AzureRmAksDashboard</span><span class="sxs-lookup"><span data-stu-id="66932-101">Start-AzureRmAksDashboard</span></span>

## <span data-ttu-id="66932-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66932-102">SYNOPSIS</span></span>
<span data-ttu-id="66932-103">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="66932-103">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66932-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66932-104">SYNTAX</span></span>

### <span data-ttu-id="66932-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="66932-105">GroupNameParameterSet (Default)</span></span>
```
Start-AzureRmAksDashboard [-ResourceGroupName] <String> [-Name] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66932-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="66932-106">InputObjectParameterSet</span></span>
```
Start-AzureRmAksDashboard [-InputObject] <PSKubernetesCluster> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66932-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="66932-107">IdParameterSet</span></span>
```
Start-AzureRmAksDashboard [-Id] <String> [-DisableBrowser] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66932-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66932-108">DESCRIPTION</span></span>
<span data-ttu-id="66932-109">Создайте туннель SSH Kubectl на панели мониторинга управляемого кластера.</span><span class="sxs-lookup"><span data-stu-id="66932-109">Create a Kubectl SSH tunnel to the managed cluster's dashboard.</span></span> <span data-ttu-id="66932-110">Настройка туннеля SSH осуществляется с помощью задания PowerShell Kubectl-Tunnel и может быть обнаружено при запуске `Get-Job` .</span><span class="sxs-lookup"><span data-stu-id="66932-110">The SSH tunnel is setup in a PowerShell job called Kubectl-Tunnel and can be found by running `Get-Job`.</span></span> <span data-ttu-id="66932-111">Туннели должны быть доступны через [http://127.0.0.1:8001](http://127.0.0.1:8001) .</span><span class="sxs-lookup"><span data-stu-id="66932-111">The tunnel should be accessable via [http://127.0.0.1:8001](http://127.0.0.1:8001).</span></span>

## <span data-ttu-id="66932-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66932-112">EXAMPLES</span></span>

### <span data-ttu-id="66932-113">Запуск туннеля SSH и открытие браузера на панели мониторинга Kubernetes</span><span class="sxs-lookup"><span data-stu-id="66932-113">Start an SSH tunnel and open a browser to the Kubernetes dashboard</span></span>
```
PS C:\> Start-AzureRmAksDashboard -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="66932-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66932-114">PARAMETERS</span></span>

### <span data-ttu-id="66932-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66932-115">-DefaultProfile</span></span>
<span data-ttu-id="66932-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66932-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66932-117">-DisableBrowser</span><span class="sxs-lookup"><span data-stu-id="66932-117">-DisableBrowser</span></span>
<span data-ttu-id="66932-118">Не выкрывайте браузер после establising kubectl порта-forward.</span><span class="sxs-lookup"><span data-stu-id="66932-118">Do not pop open a browser after establising the kubectl port-forward.</span></span>

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

### <span data-ttu-id="66932-119">-ID</span><span class="sxs-lookup"><span data-stu-id="66932-119">-Id</span></span>
<span data-ttu-id="66932-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="66932-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="66932-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66932-121">-InputObject</span></span>
<span data-ttu-id="66932-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="66932-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="66932-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66932-123">-Name</span></span>
<span data-ttu-id="66932-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="66932-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="66932-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66932-125">-PassThru</span></span>
<span data-ttu-id="66932-126">Командлет возвращает KubeTunnelJob, если он передан.</span><span class="sxs-lookup"><span data-stu-id="66932-126">Cmdlet returns the KubeTunnelJob if passed.</span></span>

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

### <span data-ttu-id="66932-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66932-127">-ResourceGroupName</span></span>
<span data-ttu-id="66932-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="66932-128">Resource group name</span></span>

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

### <span data-ttu-id="66932-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66932-129">CommonParameters</span></span>
<span data-ttu-id="66932-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66932-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66932-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66932-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66932-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66932-132">INPUTS</span></span>

### <span data-ttu-id="66932-133">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="66932-133">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="66932-134">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="66932-134">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="66932-135">System. String</span><span class="sxs-lookup"><span data-stu-id="66932-135">System.String</span></span>

## <span data-ttu-id="66932-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66932-136">OUTPUTS</span></span>

### <span data-ttu-id="66932-137">Microsoft. Azure. Commands. AKS. KubeTunnelJob</span><span class="sxs-lookup"><span data-stu-id="66932-137">Microsoft.Azure.Commands.Aks.KubeTunnelJob</span></span>

## <span data-ttu-id="66932-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="66932-138">NOTES</span></span>

## <span data-ttu-id="66932-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66932-139">RELATED LINKS</span></span>
