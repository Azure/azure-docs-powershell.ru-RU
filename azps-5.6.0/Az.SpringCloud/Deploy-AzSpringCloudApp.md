---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 96b3b3fcb2fcea50e1607c67d98079e5d1600f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955331"
---
# <span data-ttu-id="e3bf5-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="e3bf5-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="e3bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bf5-103">Развернем встроенный jar-банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="e3bf5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e3bf5-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e3bf5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="e3bf5-106">Развернем встроенный jar-банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="e3bf5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e3bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="e3bf5-108">Пример 1. Развертывание локального скомпилализованного банка для обслуживания по имени.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="e3bf5-109">Развертывание локального скомпилализованного банка для обслуживания по имени.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="e3bf5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="e3bf5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3bf5-111">-AsJob</span></span>
<span data-ttu-id="e3bf5-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="e3bf5-112">Run the command as a job</span></span>

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

### <span data-ttu-id="e3bf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bf5-113">-DefaultProfile</span></span>
<span data-ttu-id="e3bf5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3bf5-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="e3bf5-115">-JarPath</span></span>
<span data-ttu-id="e3bf5-116">Путь к банку необходимо оплести.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="e3bf5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e3bf5-117">-Name</span></span>
<span data-ttu-id="e3bf5-118">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="e3bf5-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e3bf5-119">-NoWait</span></span>
<span data-ttu-id="e3bf5-120">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="e3bf5-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e3bf5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bf5-121">-ResourceGroupName</span></span>
<span data-ttu-id="e3bf5-122">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e3bf5-123">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e3bf5-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e3bf5-124">-ServiceName</span></span>
<span data-ttu-id="e3bf5-125">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e3bf5-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3bf5-126">-SubscriptionId</span></span>
<span data-ttu-id="e3bf5-127">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3bf5-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3bf5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3bf5-129">-Confirm</span></span>
<span data-ttu-id="e3bf5-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bf5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bf5-131">-WhatIf</span></span>
<span data-ttu-id="e3bf5-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3bf5-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bf5-134">CommonParameters</span></span>
<span data-ttu-id="e3bf5-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3bf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bf5-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3bf5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bf5-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3bf5-137">INPUTS</span></span>

## <span data-ttu-id="e3bf5-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e3bf5-138">OUTPUTS</span></span>

### <span data-ttu-id="e3bf5-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="e3bf5-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="e3bf5-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e3bf5-140">NOTES</span></span>

<span data-ttu-id="e3bf5-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="e3bf5-141">ALIASES</span></span>

## <span data-ttu-id="e3bf5-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3bf5-142">RELATED LINKS</span></span>

