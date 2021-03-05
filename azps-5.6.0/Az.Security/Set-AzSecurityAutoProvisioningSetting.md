---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: b915be5c5014c278a2fbb12a6982890ed922ca60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986541"
---
# <span data-ttu-id="26e91-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="26e91-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="26e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e91-102">SYNOPSIS</span></span>
<span data-ttu-id="26e91-103">Обновляет параметр автоматической подготовка</span><span class="sxs-lookup"><span data-stu-id="26e91-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="26e91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26e91-104">SYNTAX</span></span>

### <span data-ttu-id="26e91-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26e91-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e91-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e91-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e91-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="26e91-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e91-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26e91-108">DESCRIPTION</span></span>
<span data-ttu-id="26e91-109">Включите или отключите параметры автоматической установки подписки.</span><span class="sxs-lookup"><span data-stu-id="26e91-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="26e91-110">Параметры автоматической установки по выбору центра безопасности Azure могут автоматически создать агент безопасности, который будет установлен на ваши VMs.</span><span class="sxs-lookup"><span data-stu-id="26e91-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="26e91-111">Агент безопасности будет отслеживать ваш компьютер для создания оповещений системы безопасности и соответствия требованиям.</span><span class="sxs-lookup"><span data-stu-id="26e91-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="26e91-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26e91-112">EXAMPLES</span></span>

### <span data-ttu-id="26e91-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26e91-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="26e91-114">Включает параметр автоматической подготовка для подписки.</span><span class="sxs-lookup"><span data-stu-id="26e91-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="26e91-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="26e91-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="26e91-116">Отключение автоматической настройки предварительной установки подписки.</span><span class="sxs-lookup"><span data-stu-id="26e91-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="26e91-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26e91-117">PARAMETERS</span></span>

### <span data-ttu-id="26e91-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e91-118">-DefaultProfile</span></span>
<span data-ttu-id="26e91-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26e91-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e91-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="26e91-120">-EnableAutoProvision</span></span>
<span data-ttu-id="26e91-121">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="26e91-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="26e91-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26e91-122">-InputObject</span></span>
<span data-ttu-id="26e91-123">Объект ввода.</span><span class="sxs-lookup"><span data-stu-id="26e91-123">Input Object.</span></span>

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

### <span data-ttu-id="26e91-124">-Name</span><span class="sxs-lookup"><span data-stu-id="26e91-124">-Name</span></span>
<span data-ttu-id="26e91-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="26e91-125">Resource name.</span></span>

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

### <span data-ttu-id="26e91-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26e91-126">-ResourceId</span></span>
<span data-ttu-id="26e91-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="26e91-127">Resource ID.</span></span>

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

### <span data-ttu-id="26e91-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26e91-128">-Confirm</span></span>
<span data-ttu-id="26e91-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="26e91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e91-130">-WhatIf</span></span>
<span data-ttu-id="26e91-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e91-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e91-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26e91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e91-133">CommonParameters</span></span>
<span data-ttu-id="26e91-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e91-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26e91-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e91-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26e91-136">INPUTS</span></span>

### <span data-ttu-id="26e91-137">System.String</span><span class="sxs-lookup"><span data-stu-id="26e91-137">System.String</span></span>

### <span data-ttu-id="26e91-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="26e91-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="26e91-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26e91-139">OUTPUTS</span></span>

### <span data-ttu-id="26e91-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="26e91-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="26e91-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26e91-141">NOTES</span></span>

## <span data-ttu-id="26e91-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26e91-142">RELATED LINKS</span></span>
