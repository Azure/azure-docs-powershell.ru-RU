---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244237"
---
# <span data-ttu-id="7b764-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="7b764-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="7b764-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b764-102">SYNOPSIS</span></span>
<span data-ttu-id="7b764-103">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="7b764-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="7b764-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b764-104">SYNTAX</span></span>

### <span data-ttu-id="7b764-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7b764-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b764-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7b764-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b764-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b764-107">DESCRIPTION</span></span>
<span data-ttu-id="7b764-108">Командлет **Update-AzRecoveryServicesAsrvCenter** обновляет сведения о обнаружении зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="7b764-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="7b764-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b764-109">EXAMPLES</span></span>

### <span data-ttu-id="7b764-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7b764-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="7b764-111">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="7b764-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="7b764-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b764-112">PARAMETERS</span></span>

### <span data-ttu-id="7b764-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="7b764-113">-Account</span></span>
<span data-ttu-id="7b764-114">учетные данные для входа в vCenter.</span><span class="sxs-lookup"><span data-stu-id="7b764-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="7b764-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b764-115">-DefaultProfile</span></span>
<span data-ttu-id="7b764-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7b764-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b764-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7b764-117">-InputObject</span></span>
<span data-ttu-id="7b764-118">Объект сервера vCenter, для которого нужно обновить сведения о обнаружении.</span><span class="sxs-lookup"><span data-stu-id="7b764-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="7b764-119">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="7b764-119">-Port</span></span>
<span data-ttu-id="7b764-120">Порт TCP на сервере vCenter Server, который будет использоваться для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="7b764-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="7b764-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b764-121">-ResourceId</span></span>
<span data-ttu-id="7b764-122">Указывает resourceId для vCenter.</span><span class="sxs-lookup"><span data-stu-id="7b764-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="7b764-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b764-123">-Confirm</span></span>
<span data-ttu-id="7b764-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7b764-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b764-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b764-125">-WhatIf</span></span>
<span data-ttu-id="7b764-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7b764-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b764-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7b764-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b764-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b764-128">CommonParameters</span></span>
<span data-ttu-id="7b764-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b764-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b764-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b764-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b764-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b764-131">INPUTS</span></span>

### <span data-ttu-id="7b764-132">System. String</span><span class="sxs-lookup"><span data-stu-id="7b764-132">System.String</span></span>

### <span data-ttu-id="7b764-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="7b764-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="7b764-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b764-134">OUTPUTS</span></span>

### <span data-ttu-id="7b764-135">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="7b764-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="7b764-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b764-136">NOTES</span></span>

## <span data-ttu-id="7b764-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b764-137">RELATED LINKS</span></span>
