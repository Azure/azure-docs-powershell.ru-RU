---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/set-azcloudserviceupdatedomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Set-AzCloudServiceUpdateDomain.md
ms.openlocfilehash: 4b47992eb290c0a34ac2b368017d443051a6bb92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988448"
---
# <span data-ttu-id="8525d-101">Set-AzCloudServiceUpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8525d-101">Set-AzCloudServiceUpdateDomain</span></span>

## <span data-ttu-id="8525d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8525d-102">SYNOPSIS</span></span>
<span data-ttu-id="8525d-103">Обновляет экземпляры роли в указанном домене обновления.</span><span class="sxs-lookup"><span data-stu-id="8525d-103">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="8525d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8525d-104">SYNTAX</span></span>

```
Set-AzCloudServiceUpdateDomain -CloudServiceName <String> -ResourceGroupName <String> -UpdateDomain <Int32>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8525d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8525d-105">DESCRIPTION</span></span>
<span data-ttu-id="8525d-106">Обновляет экземпляры роли в указанном домене обновления.</span><span class="sxs-lookup"><span data-stu-id="8525d-106">Updates the role instances in the specified update domain.</span></span>

## <span data-ttu-id="8525d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8525d-107">EXAMPLES</span></span>

### <span data-ttu-id="8525d-108">Пример 1. Обновление экземпляра роли в домене обновления</span><span class="sxs-lookup"><span data-stu-id="8525d-108">Example 1: Update role instance in update domain</span></span>
```powershell
PS C:\> Set-AzCloudServiceUpdateDomain -CloudServiceName "ContosoCS" -ResourceGroupName "ContosOrg" -UpdateDomain 0
```

<span data-ttu-id="8525d-109">Эта команда обновляет экземпляры ролей в домене обновления домена 0 облачной службы ContosoCS, который принадлежит к группе ресурсов ContosOrg.</span><span class="sxs-lookup"><span data-stu-id="8525d-109">This command updates role instances in update domain 0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="8525d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8525d-110">PARAMETERS</span></span>

### <span data-ttu-id="8525d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8525d-111">-AsJob</span></span>
<span data-ttu-id="8525d-112">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="8525d-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8525d-113">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="8525d-113">-CloudServiceName</span></span>
<span data-ttu-id="8525d-114">Имя облачной службы.</span><span class="sxs-lookup"><span data-stu-id="8525d-114">Name of the cloud service.</span></span>

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

### <span data-ttu-id="8525d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8525d-115">-DefaultProfile</span></span>
<span data-ttu-id="8525d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8525d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8525d-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8525d-117">-NoWait</span></span>
<span data-ttu-id="8525d-118">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="8525d-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8525d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8525d-119">-PassThru</span></span>
<span data-ttu-id="8525d-120">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="8525d-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8525d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8525d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8525d-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8525d-122">Name of the resource group.</span></span>

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

### <span data-ttu-id="8525d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8525d-123">-SubscriptionId</span></span>
<span data-ttu-id="8525d-124">Учетные данные подписки, однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8525d-124">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8525d-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8525d-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8525d-126">-UpdateDomain</span><span class="sxs-lookup"><span data-stu-id="8525d-126">-UpdateDomain</span></span>
<span data-ttu-id="8525d-127">Указывает значение, определя которое определяет домен обновления.</span><span class="sxs-lookup"><span data-stu-id="8525d-127">Specifies an integer value that identifies the update domain.</span></span>
<span data-ttu-id="8525d-128">Домены обновления имеют индекс с нулевым индексом: у первого домена обновления — 0, у второго — 1 и так далее.</span><span class="sxs-lookup"><span data-stu-id="8525d-128">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8525d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8525d-129">-Confirm</span></span>
<span data-ttu-id="8525d-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8525d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8525d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8525d-131">-WhatIf</span></span>
<span data-ttu-id="8525d-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8525d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8525d-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8525d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8525d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8525d-134">CommonParameters</span></span>
<span data-ttu-id="8525d-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8525d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8525d-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8525d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8525d-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8525d-137">INPUTS</span></span>

## <span data-ttu-id="8525d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8525d-138">OUTPUTS</span></span>

### <span data-ttu-id="8525d-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8525d-139">System.Boolean</span></span>

## <span data-ttu-id="8525d-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8525d-140">NOTES</span></span>

<span data-ttu-id="8525d-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8525d-141">ALIASES</span></span>

## <span data-ttu-id="8525d-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8525d-142">RELATED LINKS</span></span>

