---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: c6a7381c993b52995ab39a60fde54900092a5915
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517149"
---
# <span data-ttu-id="95db1-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="95db1-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="95db1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95db1-102">SYNOPSIS</span></span>
<span data-ttu-id="95db1-103">Развернем встроенный jar-банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="95db1-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="95db1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="95db1-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="95db1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95db1-105">DESCRIPTION</span></span>
<span data-ttu-id="95db1-106">Развернем встроенный jar-банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="95db1-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="95db1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="95db1-107">EXAMPLES</span></span>

### <span data-ttu-id="95db1-108">Пример 1. Развертывание локального скомпилализованного банка для обслуживания по имени.</span><span class="sxs-lookup"><span data-stu-id="95db1-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="95db1-109">Развертывание локального скомпилализованного банка для обслуживания по имени.</span><span class="sxs-lookup"><span data-stu-id="95db1-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="95db1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="95db1-110">PARAMETERS</span></span>

### <span data-ttu-id="95db1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95db1-111">-AsJob</span></span>
<span data-ttu-id="95db1-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="95db1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="95db1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95db1-113">-DefaultProfile</span></span>
<span data-ttu-id="95db1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95db1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95db1-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="95db1-115">-JarPath</span></span>
<span data-ttu-id="95db1-116">Путь к банку необходимо оплести.</span><span class="sxs-lookup"><span data-stu-id="95db1-116">The path of the jar need to be deploied.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95db1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="95db1-117">-Name</span></span>
<span data-ttu-id="95db1-118">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="95db1-118">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95db1-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="95db1-119">-NoWait</span></span>
<span data-ttu-id="95db1-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="95db1-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95db1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95db1-121">-ResourceGroupName</span></span>
<span data-ttu-id="95db1-122">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="95db1-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="95db1-123">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="95db1-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95db1-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="95db1-124">-ServiceName</span></span>
<span data-ttu-id="95db1-125">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="95db1-125">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95db1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95db1-126">-SubscriptionId</span></span>
<span data-ttu-id="95db1-127">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95db1-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="95db1-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="95db1-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95db1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95db1-129">-Confirm</span></span>
<span data-ttu-id="95db1-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95db1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95db1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95db1-131">-WhatIf</span></span>
<span data-ttu-id="95db1-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="95db1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95db1-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="95db1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95db1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95db1-134">CommonParameters</span></span>
<span data-ttu-id="95db1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95db1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95db1-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="95db1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95db1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="95db1-137">INPUTS</span></span>

## <span data-ttu-id="95db1-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="95db1-138">OUTPUTS</span></span>

### <span data-ttu-id="95db1-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="95db1-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="95db1-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="95db1-140">NOTES</span></span>

<span data-ttu-id="95db1-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="95db1-141">ALIASES</span></span>

## <span data-ttu-id="95db1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95db1-142">RELATED LINKS</span></span>

