---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248016"
---
# <span data-ttu-id="4ea5a-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="4ea5a-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4ea5a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ea5a-102">SYNOPSIS</span></span>
<span data-ttu-id="4ea5a-103">Получает параметры автоматического обеспечения безопасности</span><span class="sxs-lookup"><span data-stu-id="4ea5a-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="4ea5a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ea5a-104">SYNTAX</span></span>

### <span data-ttu-id="4ea5a-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ea5a-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ea5a-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4ea5a-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ea5a-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ea5a-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4ea5a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea5a-108">DESCRIPTION</span></span>
<span data-ttu-id="4ea5a-109">Параметры автоматической подготовки позволяют решить, должен ли центр безопасности Azure автоматически подготавливать агент безопасности, который будет установлен на ваших виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="4ea5a-110">Агент безопасности будет наблюдать за виртуальной машиной для создания оповещений системы безопасности и отслеживания соответствия требованиям безопасности виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="4ea5a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ea5a-111">EXAMPLES</span></span>

### <span data-ttu-id="4ea5a-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ea5a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="4ea5a-113">Получает параметр автоматической подготовки для подписки.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="4ea5a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ea5a-114">PARAMETERS</span></span>

### <span data-ttu-id="4ea5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ea5a-115">-DefaultProfile</span></span>
<span data-ttu-id="4ea5a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ea5a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ea5a-117">-Name</span></span>
<span data-ttu-id="4ea5a-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-118">Resource name.</span></span>

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

### <span data-ttu-id="4ea5a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ea5a-119">-ResourceId</span></span>
<span data-ttu-id="4ea5a-120">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-120">Resource ID.</span></span>

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

### <span data-ttu-id="4ea5a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ea5a-121">CommonParameters</span></span>
<span data-ttu-id="4ea5a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ea5a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ea5a-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ea5a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ea5a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ea5a-124">INPUTS</span></span>

### <span data-ttu-id="4ea5a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="4ea5a-125">System.String</span></span>

## <span data-ttu-id="4ea5a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ea5a-126">OUTPUTS</span></span>

### <span data-ttu-id="4ea5a-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="4ea5a-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="4ea5a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ea5a-128">NOTES</span></span>

## <span data-ttu-id="4ea5a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ea5a-129">RELATED LINKS</span></span>