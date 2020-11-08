---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/deploy-azSpringCloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Deploy-AzSpringCloudApp.md
ms.openlocfilehash: 8a80c323f1cf1d8d015faeda6541b77667a6ca19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235844"
---
# <span data-ttu-id="c776b-101">Deploy-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="c776b-101">Deploy-AzSpringCloudApp</span></span>

## <span data-ttu-id="c776b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c776b-102">SYNOPSIS</span></span>
<span data-ttu-id="c776b-103">Разверните созданный банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c776b-103">Deploy the built jar to service.</span></span>

## <span data-ttu-id="c776b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c776b-104">SYNTAX</span></span>

```
Deploy-AzSpringCloudApp -JarPath <String> -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c776b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c776b-105">DESCRIPTION</span></span>
<span data-ttu-id="c776b-106">Разверните созданный банк для обслуживания.</span><span class="sxs-lookup"><span data-stu-id="c776b-106">Deploy the built jar to service.</span></span>

## <span data-ttu-id="c776b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c776b-107">EXAMPLES</span></span>

### <span data-ttu-id="c776b-108">Пример 1: развертывание локального скомпилированного JAR для службы по имени.</span><span class="sxs-lookup"><span data-stu-id="c776b-108">Example 1: Deploy local compiled jar to service by name.</span></span>
```powershell
PS C:\> Deploy-AzSpringCloudApp -ResourceGroupName 'spring-cloud-rg' -ServiceName 'spring-cloud-service' -AppName 'gateway' -JarPath '/home/user/piggymetrics/gateway/target/gateway.jar'

[1/3] Requesting for upload URL
[2/3] Uploading package to blob
[3/3] Updating deployment in app account-service (this operation can take a while to complete)
Name Type
---- ----
prod Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="c776b-109">Развертывание локальных скомпилированных JAR для службы по имени.</span><span class="sxs-lookup"><span data-stu-id="c776b-109">Deploy local compiled jar to service by name.</span></span>

## <span data-ttu-id="c776b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c776b-110">PARAMETERS</span></span>

### <span data-ttu-id="c776b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c776b-111">-AsJob</span></span>
<span data-ttu-id="c776b-112">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c776b-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c776b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c776b-113">-DefaultProfile</span></span>
<span data-ttu-id="c776b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c776b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c776b-115">-JarPath</span><span class="sxs-lookup"><span data-stu-id="c776b-115">-JarPath</span></span>
<span data-ttu-id="c776b-116">Путь к банку данных должен быть deploied.</span><span class="sxs-lookup"><span data-stu-id="c776b-116">The path of the jar need to be deploied.</span></span>

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

### <span data-ttu-id="c776b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c776b-117">-Name</span></span>
<span data-ttu-id="c776b-118">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="c776b-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="c776b-119">-Wait</span><span class="sxs-lookup"><span data-stu-id="c776b-119">-NoWait</span></span>
<span data-ttu-id="c776b-120">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="c776b-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c776b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c776b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c776b-122">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="c776b-122">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c776b-123">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c776b-123">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c776b-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c776b-124">-ServiceName</span></span>
<span data-ttu-id="c776b-125">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="c776b-125">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c776b-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c776b-126">-SubscriptionId</span></span>
<span data-ttu-id="c776b-127">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c776b-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c776b-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="c776b-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c776b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c776b-129">-Confirm</span></span>
<span data-ttu-id="c776b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c776b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c776b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c776b-131">-WhatIf</span></span>
<span data-ttu-id="c776b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c776b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c776b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c776b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c776b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c776b-134">CommonParameters</span></span>
<span data-ttu-id="c776b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c776b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c776b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c776b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c776b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c776b-137">INPUTS</span></span>

## <span data-ttu-id="c776b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c776b-138">OUTPUTS</span></span>

### <span data-ttu-id="c776b-139">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20190501Preview. IAppResource</span><span class="sxs-lookup"><span data-stu-id="c776b-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="c776b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="c776b-140">NOTES</span></span>

<span data-ttu-id="c776b-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="c776b-141">ALIASES</span></span>

## <span data-ttu-id="c776b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c776b-142">RELATED LINKS</span></span>

