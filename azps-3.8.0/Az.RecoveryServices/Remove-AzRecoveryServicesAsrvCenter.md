---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 775a8694df895601d953a1efd68b7a4cba57a830
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072625"
---
# <span data-ttu-id="512b2-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="512b2-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="512b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="512b2-102">SYNOPSIS</span></span>
<span data-ttu-id="512b2-103">Удаляет vCenter Server из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="512b2-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="512b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="512b2-104">SYNTAX</span></span>

### <span data-ttu-id="512b2-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="512b2-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="512b2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="512b2-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="512b2-107">ByName</span><span class="sxs-lookup"><span data-stu-id="512b2-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512b2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="512b2-108">DESCRIPTION</span></span>
<span data-ttu-id="512b2-109">Командлет **Remove-AzRecoveryServicesAsrvCenter** удаляет сервер vCenter из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="512b2-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="512b2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="512b2-110">EXAMPLES</span></span>

### <span data-ttu-id="512b2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="512b2-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="512b2-112">Удаляет vCenter Server из структуры ASR.</span><span class="sxs-lookup"><span data-stu-id="512b2-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="512b2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="512b2-113">PARAMETERS</span></span>

### <span data-ttu-id="512b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512b2-114">-DefaultProfile</span></span>
<span data-ttu-id="512b2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="512b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="512b2-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="512b2-116">-Fabric</span></span>
<span data-ttu-id="512b2-117">Объект Fabric ASR, представляющий сервер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="512b2-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="512b2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="512b2-118">-InputObject</span></span>
<span data-ttu-id="512b2-119">Объект ASR vCenter, представляющий сервер vCenter Server, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="512b2-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="512b2-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="512b2-120">-Name</span></span>
<span data-ttu-id="512b2-121">Имя сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="512b2-121">Name of the vCenter Server.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="512b2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="512b2-122">-ResourceId</span></span>
<span data-ttu-id="512b2-123">Указывает ИД ресурса vCenter, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="512b2-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="512b2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="512b2-124">-Confirm</span></span>
<span data-ttu-id="512b2-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="512b2-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512b2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512b2-126">-WhatIf</span></span>
<span data-ttu-id="512b2-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="512b2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512b2-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="512b2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512b2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512b2-129">CommonParameters</span></span>
<span data-ttu-id="512b2-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="512b2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512b2-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="512b2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512b2-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="512b2-132">INPUTS</span></span>

### <span data-ttu-id="512b2-133">System. String</span><span class="sxs-lookup"><span data-stu-id="512b2-133">System.String</span></span>

### <span data-ttu-id="512b2-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="512b2-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="512b2-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="512b2-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="512b2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="512b2-136">OUTPUTS</span></span>

### <span data-ttu-id="512b2-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="512b2-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="512b2-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="512b2-138">NOTES</span></span>

## <span data-ttu-id="512b2-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="512b2-139">RELATED LINKS</span></span>
