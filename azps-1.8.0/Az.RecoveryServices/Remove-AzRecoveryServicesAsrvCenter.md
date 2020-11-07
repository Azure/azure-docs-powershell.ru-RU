---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: c1ac3ae34e92feb2b356d5946a7b9f0a30a0a2aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729624"
---
# <span data-ttu-id="4e8ea-101">Remove-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="4e8ea-101">Remove-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="4e8ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="4e8ea-103">Удаляет vCenter Server из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="4e8ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e8ea-104">SYNTAX</span></span>

### <span data-ttu-id="4e8ea-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e8ea-105">Default (Default)</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e8ea-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e8ea-106">ByResourceId</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e8ea-107">ByName</span><span class="sxs-lookup"><span data-stu-id="4e8ea-107">ByName</span></span>
```
Remove-AzRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e8ea-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e8ea-108">DESCRIPTION</span></span>
<span data-ttu-id="4e8ea-109">Командлет **Remove-AzRecoveryServicesAsrvCenter** удаляет сервер vCenter из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-109">The **Remove-AzRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="4e8ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e8ea-110">EXAMPLES</span></span>

### <span data-ttu-id="4e8ea-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e8ea-111">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="4e8ea-112">Удаляет vCenter Server из структуры ASR.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="4e8ea-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e8ea-113">PARAMETERS</span></span>

### <span data-ttu-id="4e8ea-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e8ea-114">-DefaultProfile</span></span>
<span data-ttu-id="4e8ea-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e8ea-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="4e8ea-116">-Fabric</span></span>
<span data-ttu-id="4e8ea-117">Объект Fabric ASR, представляющий сервер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-117">ASR fabric object representing the Configuration Server.</span></span>

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

### <span data-ttu-id="4e8ea-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e8ea-118">-InputObject</span></span>
<span data-ttu-id="4e8ea-119">Объект ASR vCenter, представляющий сервер vCenter Server, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

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

### <span data-ttu-id="4e8ea-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e8ea-120">-Name</span></span>
<span data-ttu-id="4e8ea-121">Имя сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="4e8ea-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e8ea-122">-ResourceId</span></span>
<span data-ttu-id="4e8ea-123">Указывает ИД ресурса vCenter, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-123">Specifies the resourceId of vCenter to remove.</span></span>

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

### <span data-ttu-id="4e8ea-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e8ea-124">-Confirm</span></span>
<span data-ttu-id="4e8ea-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e8ea-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e8ea-126">-WhatIf</span></span>
<span data-ttu-id="4e8ea-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e8ea-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e8ea-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e8ea-129">CommonParameters</span></span>
<span data-ttu-id="4e8ea-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e8ea-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e8ea-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e8ea-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e8ea-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e8ea-132">INPUTS</span></span>

### <span data-ttu-id="4e8ea-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4e8ea-133">System.String</span></span>

### <span data-ttu-id="4e8ea-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="4e8ea-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

### <span data-ttu-id="4e8ea-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="4e8ea-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4e8ea-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e8ea-136">OUTPUTS</span></span>

### <span data-ttu-id="4e8ea-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4e8ea-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4e8ea-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e8ea-138">NOTES</span></span>

## <span data-ttu-id="4e8ea-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e8ea-139">RELATED LINKS</span></span>
