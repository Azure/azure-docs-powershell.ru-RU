---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: e99ead17cad0a3c6c440967ec1b1852bb5568a26
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732580"
---
# <span data-ttu-id="42a6d-101">Set-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="42a6d-101">Set-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="42a6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="42a6d-103">Автоматическое обновление параметров подготовки</span><span class="sxs-lookup"><span data-stu-id="42a6d-103">Updates automatic provisioning setting</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42a6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42a6d-104">SYNTAX</span></span>

### <span data-ttu-id="42a6d-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42a6d-105">SubscriptionLevelResource (Default)</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -Name <String> [-EnableAutoProvision]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a6d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a6d-106">ResourceId</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting [-EnableAutoProvision] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a6d-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="42a6d-107">InputObject</span></span>
```
Set-AzureRmSecurityAutoProvisioningSetting -InputObject <PSSecurityAutoProvisioningSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a6d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42a6d-108">DESCRIPTION</span></span>
<span data-ttu-id="42a6d-109">Включение и отключение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="42a6d-109">Turns on or off automatic provisioning settings for a subscription.</span></span>
<span data-ttu-id="42a6d-110">Параметры автоматической подготовки позволяют решить, должен ли центр безопасности Azure автоматически подготавливать агент безопасности, который будет установлен на ваших виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="42a6d-110">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="42a6d-111">Агент безопасности будет наблюдать за виртуальной машиной для создания оповещений системы безопасности и отслеживания соответствия требованиям безопасности виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="42a6d-111">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="42a6d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42a6d-112">EXAMPLES</span></span>

### <span data-ttu-id="42a6d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42a6d-113">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default" -EnableAutoProvision
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="42a6d-114">Включение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="42a6d-114">Turns on automatic provisioning setting for a subscription.</span></span>

### <span data-ttu-id="42a6d-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42a6d-115">Example 2</span></span>
```powershell
PS C:\> Set-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name 
--                                                                                                                ---- 
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default de...
```

<span data-ttu-id="42a6d-116">Отключение автоматической настройки подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="42a6d-116">Turns off automatic provisioning setting for a subscription.</span></span>

## <span data-ttu-id="42a6d-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42a6d-117">PARAMETERS</span></span>

### <span data-ttu-id="42a6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42a6d-118">-DefaultProfile</span></span>
<span data-ttu-id="42a6d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42a6d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-120">-EnableAutoProvision</span><span class="sxs-lookup"><span data-stu-id="42a6d-120">-EnableAutoProvision</span></span>
<span data-ttu-id="42a6d-121">Автоматическая подготовка.</span><span class="sxs-lookup"><span data-stu-id="42a6d-121">Automatic Provisioning.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SubscriptionLevelResource, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42a6d-122">-InputObject</span></span>
<span data-ttu-id="42a6d-123">Объект input.</span><span class="sxs-lookup"><span data-stu-id="42a6d-123">Input Object.</span></span>

```yaml
Type: PSSecurityAutoProvisioningSetting
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42a6d-124">-Name</span></span>
<span data-ttu-id="42a6d-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="42a6d-125">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a6d-126">-ResourceId</span></span>
<span data-ttu-id="42a6d-127">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="42a6d-127">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42a6d-128">-Confirm</span></span>
<span data-ttu-id="42a6d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42a6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a6d-130">-WhatIf</span></span>
<span data-ttu-id="42a6d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="42a6d-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42a6d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="42a6d-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a6d-133">CommonParameters</span></span>
<span data-ttu-id="42a6d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42a6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a6d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a6d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a6d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42a6d-136">INPUTS</span></span>

### <span data-ttu-id="42a6d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="42a6d-137">System.String</span></span>
<span data-ttu-id="42a6d-138">System. Management. Automation. SwitchParameter Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="42a6d-138">System.Management.Automation.SwitchParameter Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="42a6d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42a6d-139">OUTPUTS</span></span>

### <span data-ttu-id="42a6d-140">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="42a6d-140">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="42a6d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="42a6d-141">NOTES</span></span>

## <span data-ttu-id="42a6d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42a6d-142">RELATED LINKS</span></span>
