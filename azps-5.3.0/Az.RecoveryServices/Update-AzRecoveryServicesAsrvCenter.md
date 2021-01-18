---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrvCenter.md
ms.openlocfilehash: 9e4ee275bf003dfa011eba4f00aad0029b5152de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505400"
---
# <span data-ttu-id="5fef9-101">Update-AzRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="5fef9-101">Update-AzRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="5fef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5fef9-102">SYNOPSIS</span></span>
<span data-ttu-id="5fef9-103">Обновление сведений об обнаружении для зарегистрированного центра vCenter.</span><span class="sxs-lookup"><span data-stu-id="5fef9-103">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="5fef9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5fef9-104">SYNTAX</span></span>

### <span data-ttu-id="5fef9-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fef9-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fef9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5fef9-106">ByResourceId</span></span>
```
Update-AzRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fef9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fef9-107">DESCRIPTION</span></span>
<span data-ttu-id="5fef9-108">Для **зарегистрированного центра обновления azRecoveryServicesAsrvCenter** обновляется информация об обнаружении.</span><span class="sxs-lookup"><span data-stu-id="5fef9-108">The **Update-AzRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="5fef9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5fef9-109">EXAMPLES</span></span>

### <span data-ttu-id="5fef9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fef9-110">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="5fef9-111">Обновление сведений об обнаружении для зарегистрированного центра vCenter.</span><span class="sxs-lookup"><span data-stu-id="5fef9-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="5fef9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5fef9-112">PARAMETERS</span></span>

### <span data-ttu-id="5fef9-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5fef9-113">-Account</span></span>
<span data-ttu-id="5fef9-114">учетная запись для входа в vCenter.</span><span class="sxs-lookup"><span data-stu-id="5fef9-114">vCenter login credentials account.</span></span>

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

### <span data-ttu-id="5fef9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fef9-115">-DefaultProfile</span></span>
<span data-ttu-id="5fef9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fef9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fef9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5fef9-117">-InputObject</span></span>
<span data-ttu-id="5fef9-118">Объект сервера vCenter, для обновления сведений об обнаружении.</span><span class="sxs-lookup"><span data-stu-id="5fef9-118">The vCenter server object to update discovery details for.</span></span>

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

### <span data-ttu-id="5fef9-119">-Port</span><span class="sxs-lookup"><span data-stu-id="5fef9-119">-Port</span></span>
<span data-ttu-id="5fef9-120">Порт TCP на сервере vCenter, который нужно использовать для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="5fef9-120">The TCP port on the vCenter server to use for discovery.</span></span>

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

### <span data-ttu-id="5fef9-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5fef9-121">-ResourceId</span></span>
<span data-ttu-id="5fef9-122">Определяет ид ресурса vCenter.</span><span class="sxs-lookup"><span data-stu-id="5fef9-122">Specifies the resourceId of vCenter.</span></span>

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

### <span data-ttu-id="5fef9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fef9-123">-Confirm</span></span>
<span data-ttu-id="5fef9-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fef9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fef9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fef9-125">-WhatIf</span></span>
<span data-ttu-id="5fef9-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fef9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fef9-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5fef9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fef9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fef9-128">CommonParameters</span></span>
<span data-ttu-id="5fef9-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fef9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fef9-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5fef9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fef9-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5fef9-131">INPUTS</span></span>

### <span data-ttu-id="5fef9-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5fef9-132">System.String</span></span>

### <span data-ttu-id="5fef9-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="5fef9-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="5fef9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5fef9-134">OUTPUTS</span></span>

### <span data-ttu-id="5fef9-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5fef9-135">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5fef9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5fef9-136">NOTES</span></span>

## <span data-ttu-id="5fef9-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fef9-137">RELATED LINKS</span></span>
