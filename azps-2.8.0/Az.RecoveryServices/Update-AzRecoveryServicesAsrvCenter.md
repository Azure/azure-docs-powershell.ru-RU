---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: d6e26eb293a2b87fccc0749b6d5c53d15d7d860f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905749"
---
# <span data-ttu-id="0469f-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="0469f-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="0469f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0469f-102">SYNOPSIS</span></span>
<span data-ttu-id="0469f-103">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="0469f-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="0469f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0469f-104">SYNTAX</span></span>

### <span data-ttu-id="0469f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0469f-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0469f-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0469f-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0469f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0469f-107">DESCRIPTION</span></span>
<span data-ttu-id="0469f-108">Командлет **Update-AzRecoveryServicesAsrvCenter** обновляет сведения о обнаружении зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="0469f-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="0469f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0469f-109">EXAMPLES</span></span>

### <span data-ttu-id="0469f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0469f-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="0469f-111">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="0469f-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="0469f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0469f-112">PARAMETERS</span></span>

### <span data-ttu-id="0469f-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="0469f-113">-Account</span></span>
<span data-ttu-id="0469f-114">учетные данные для входа в vCenter.</span><span class="sxs-lookup"><span data-stu-id="0469f-114">vCenter login credentials account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0469f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0469f-115">-DefaultProfile</span></span>
<span data-ttu-id="0469f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0469f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0469f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0469f-117">-InputObject</span></span>
<span data-ttu-id="0469f-118">Объект сервера vCenter, для которого нужно обновить сведения о обнаружении.</span><span class="sxs-lookup"><span data-stu-id="0469f-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="0469f-119">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="0469f-119">-Port</span></span>
<span data-ttu-id="0469f-120">Порт TCP на сервере vCenter Server, который будет использоваться для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="0469f-120">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0469f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0469f-121">-ResourceId</span></span>
<span data-ttu-id="0469f-122">Указывает resourceId для vCenter.</span><span class="sxs-lookup"><span data-stu-id="0469f-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="0469f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0469f-123">-Confirm</span></span>
<span data-ttu-id="0469f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0469f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0469f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0469f-125">-WhatIf</span></span>
<span data-ttu-id="0469f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0469f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0469f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0469f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0469f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0469f-128">CommonParameters</span></span>
<span data-ttu-id="0469f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0469f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0469f-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0469f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0469f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0469f-131">INPUTS</span></span>

### <span data-ttu-id="0469f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0469f-132">System.String</span></span>

### <span data-ttu-id="0469f-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="0469f-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="0469f-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0469f-134">OUTPUTS</span></span>

### <span data-ttu-id="0469f-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0469f-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0469f-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="0469f-136">NOTES</span></span>

## <span data-ttu-id="0469f-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0469f-137">RELATED LINKS</span></span>
