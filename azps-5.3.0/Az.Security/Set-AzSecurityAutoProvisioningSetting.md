---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: f3d30608230fffc934a3cfcf9a4b15264dbcf008
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517641"
---
# <span data-ttu-id="91d9b-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="91d9b-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="91d9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91d9b-102">SYNOPSIS</span></span>
<span data-ttu-id="91d9b-103">Обновляет параметр автоматической подготовка</span><span class="sxs-lookup"><span data-stu-id="91d9b-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="91d9b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="91d9b-104">SYNTAX</span></span>

### <span data-ttu-id="91d9b-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="91d9b-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d9b-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="91d9b-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91d9b-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="91d9b-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91d9b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="91d9b-108">DESCRIPTION</span></span>
<span data-ttu-id="91d9b-109">Включите или отключите параметры автоматической установки подписки.</span><span class="sxs-lookup"><span data-stu-id="91d9b-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="91d9b-110">Параметры автоматической установки по выбору центра безопасности Azure могут автоматически создать агент безопасности, который будет устанавливаться на ваши VMs.</span><span class="sxs-lookup"><span data-stu-id="91d9b-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="91d9b-111">Агент безопасности будет отслеживать VM-компьютер для создания оповещений системы безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="91d9b-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="91d9b-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="91d9b-112">EXAMPLES</span></span>

### <span data-ttu-id="91d9b-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="91d9b-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="91d9b-114">Включает параметр автоматической подготовка подписки.</span><span class="sxs-lookup"><span data-stu-id="91d9b-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="91d9b-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="91d9b-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="91d9b-116">Отключается автоматическая подготовка подписки.</span><span class="sxs-lookup"><span data-stu-id="91d9b-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="91d9b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91d9b-117">PARAMETERS</span></span>

### <span data-ttu-id="91d9b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d9b-118">-DefaultProfile</span></span>
<span data-ttu-id="91d9b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="91d9b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91d9b-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="91d9b-120">-EnableAutoProvision</span></span>
<span data-ttu-id="91d9b-121">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="91d9b-121">Automatic Provisioning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d9b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91d9b-122">-InputObject</span></span>
<span data-ttu-id="91d9b-123">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="91d9b-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91d9b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="91d9b-124">-Name</span></span>
<span data-ttu-id="91d9b-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="91d9b-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91d9b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91d9b-126">-ResourceId</span></span>
<span data-ttu-id="91d9b-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="91d9b-127">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91d9b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="91d9b-128">-Confirm</span></span>
<span data-ttu-id="91d9b-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91d9b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d9b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d9b-130">-WhatIf</span></span>
<span data-ttu-id="91d9b-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91d9b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91d9b-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="91d9b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91d9b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d9b-133">CommonParameters</span></span>
<span data-ttu-id="91d9b-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d9b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d9b-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91d9b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d9b-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="91d9b-136">INPUTS</span></span>

### <span data-ttu-id="91d9b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="91d9b-137">System.String</span></span>

### <span data-ttu-id="91d9b-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="91d9b-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="91d9b-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="91d9b-139">OUTPUTS</span></span>

### <span data-ttu-id="91d9b-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="91d9b-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="91d9b-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="91d9b-141">NOTES</span></span>

## <span data-ttu-id="91d9b-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="91d9b-142">RELATED LINKS</span></span>
