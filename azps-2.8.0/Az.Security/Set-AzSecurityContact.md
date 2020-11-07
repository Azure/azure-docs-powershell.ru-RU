---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 1bf9e6b51899054899e819784872cf688a182e16
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905409"
---
# <span data-ttu-id="be762-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="be762-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="be762-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be762-102">SYNOPSIS</span></span>
<span data-ttu-id="be762-103">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="be762-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="be762-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be762-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be762-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be762-105">DESCRIPTION</span></span>
<span data-ttu-id="be762-106">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="be762-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="be762-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be762-107">EXAMPLES</span></span>

### <span data-ttu-id="be762-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be762-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="be762-109">Обновляет контакт безопасности для подписки.</span><span class="sxs-lookup"><span data-stu-id="be762-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="be762-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be762-110">PARAMETERS</span></span>

### <span data-ttu-id="be762-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="be762-111">-AlertAdmin</span></span>
<span data-ttu-id="be762-112">Оповещения для администраторов.</span><span class="sxs-lookup"><span data-stu-id="be762-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be762-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be762-113">-DefaultProfile</span></span>
<span data-ttu-id="be762-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be762-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be762-115">-Электронная почта</span><span class="sxs-lookup"><span data-stu-id="be762-115">-Email</span></span>
<span data-ttu-id="be762-116">Почтов.</span><span class="sxs-lookup"><span data-stu-id="be762-116">E-Mail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be762-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be762-117">-Name</span></span>
<span data-ttu-id="be762-118">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="be762-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be762-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="be762-119">-NotifyOnAlert</span></span>
<span data-ttu-id="be762-120">Уведомления о предупреждениях.</span><span class="sxs-lookup"><span data-stu-id="be762-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be762-121">-Phone</span><span class="sxs-lookup"><span data-stu-id="be762-121">-Phone</span></span>
<span data-ttu-id="be762-122">Кнопка.</span><span class="sxs-lookup"><span data-stu-id="be762-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be762-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be762-123">-Confirm</span></span>
<span data-ttu-id="be762-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be762-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be762-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be762-125">-WhatIf</span></span>
<span data-ttu-id="be762-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be762-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be762-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be762-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be762-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be762-128">CommonParameters</span></span>
<span data-ttu-id="be762-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be762-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be762-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be762-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be762-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be762-131">INPUTS</span></span>

### <span data-ttu-id="be762-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="be762-132">None</span></span>

## <span data-ttu-id="be762-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be762-133">OUTPUTS</span></span>

### <span data-ttu-id="be762-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="be762-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="be762-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="be762-135">NOTES</span></span>

## <span data-ttu-id="be762-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be762-136">RELATED LINKS</span></span>
