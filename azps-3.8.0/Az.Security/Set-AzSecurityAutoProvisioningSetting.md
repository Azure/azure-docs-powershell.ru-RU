---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 4a54b75ce8f9361957202633c70d00431c7bdb8c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073773"
---
# <span data-ttu-id="449c8-101">Set-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="449c8-101">Set-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="449c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="449c8-102">SYNOPSIS</span></span>
<span data-ttu-id="449c8-103">Автоматическое обновление параметров подготовки</span><span class="sxs-lookup"><span data-stu-id="449c8-103">Updates automatic provisioning setting</span></span>

## <span data-ttu-id="449c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="449c8-104">SYNTAX</span></span>

### <span data-ttu-id="449c8-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="449c8-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449c8-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="449c8-106">ResourceId</span></span>
```
Set-AzSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="449c8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="449c8-107">InputObject</span></span>
```
Set-AzSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="449c8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="449c8-108">DESCRIPTION</span></span>
<span data-ttu-id="449c8-109">Включение и отключение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="449c8-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="449c8-110">Параметры автоматической подготовки позволяют решить, должен ли центр безопасности Azure автоматически подготавливать агент безопасности, который будет установлен на ваших виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="449c8-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="449c8-111">Агент безопасности будет наблюдать за виртуальной машиной для создания оповещений системы безопасности и отслеживания соответствия требованиям безопасности виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="449c8-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="449c8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="449c8-112">EXAMPLES</span></span>

### <span data-ttu-id="449c8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="449c8-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="449c8-114">Включение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="449c8-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="449c8-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="449c8-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="449c8-116">Отключение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="449c8-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="449c8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="449c8-117">PARAMETERS</span></span>

### <span data-ttu-id="449c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="449c8-118">-DefaultProfile</span></span>
<span data-ttu-id="449c8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="449c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="449c8-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="449c8-120">-EnableAutoProvision</span></span>
<span data-ttu-id="449c8-121">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="449c8-121">Automatic Provisioning.</span></span>

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

### <span data-ttu-id="449c8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="449c8-122">-InputObject</span></span>
<span data-ttu-id="449c8-123">Объект input.</span><span class="sxs-lookup"><span data-stu-id="449c8-123">Input Object.</span></span>

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

### <span data-ttu-id="449c8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="449c8-124">-Name</span></span>
<span data-ttu-id="449c8-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="449c8-125">Resource name.</span></span>

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

### <span data-ttu-id="449c8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="449c8-126">-ResourceId</span></span>
<span data-ttu-id="449c8-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="449c8-127">Resource ID.</span></span>

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

### <span data-ttu-id="449c8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="449c8-128">-Confirm</span></span>
<span data-ttu-id="449c8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="449c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="449c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="449c8-130">-WhatIf</span></span>
<span data-ttu-id="449c8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="449c8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="449c8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="449c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="449c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="449c8-133">CommonParameters</span></span>
<span data-ttu-id="449c8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="449c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="449c8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="449c8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="449c8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="449c8-136">INPUTS</span></span>

### <span data-ttu-id="449c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="449c8-137">System.String</span></span>

### <span data-ttu-id="449c8-138">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="449c8-138">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="449c8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="449c8-139">OUTPUTS</span></span>

### <span data-ttu-id="449c8-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="449c8-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="449c8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="449c8-141">NOTES</span></span>

## <span data-ttu-id="449c8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="449c8-142">RELATED LINKS</span></span>
