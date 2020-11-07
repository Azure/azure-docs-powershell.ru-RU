---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzSecurityContact.md
ms.openlocfilehash: eac99fc2395408f2e140b3369a87e75928006f21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903893"
---
# <span data-ttu-id="df5d6-101">Remove-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="df5d6-101">Remove-AzSecurityContact</span></span>

## <span data-ttu-id="df5d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df5d6-102">SYNOPSIS</span></span>
<span data-ttu-id="df5d6-103">Удаление контакта безопасности.</span><span class="sxs-lookup"><span data-stu-id="df5d6-103">Deletes a security contact.</span></span>

## <span data-ttu-id="df5d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df5d6-104">SYNTAX</span></span>

### <span data-ttu-id="df5d6-105">SubscriptionLevelResource (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df5d6-105">SubscriptionLevelResource (Default)</span></span>
```
Remove-AzSecurityContact -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df5d6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5d6-106">ResourceId</span></span>
```
Remove-AzSecurityContact -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df5d6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="df5d6-107">InputObject</span></span>
```
Remove-AzSecurityContact -InputObject <PSSecurityContact> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df5d6-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df5d6-108">DESCRIPTION</span></span>
<span data-ttu-id="df5d6-109">Удаление контакта безопасности.</span><span class="sxs-lookup"><span data-stu-id="df5d6-109">Deletes a security contact.</span></span>

## <span data-ttu-id="df5d6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df5d6-110">EXAMPLES</span></span>

### <span data-ttu-id="df5d6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="df5d6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSecurityContact -Name "default1"
```

<span data-ttu-id="df5d6-112">Удаляет контакт безопасности "default1"</span><span class="sxs-lookup"><span data-stu-id="df5d6-112">Deletes the "default1" security contact</span></span>

## <span data-ttu-id="df5d6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df5d6-113">PARAMETERS</span></span>

### <span data-ttu-id="df5d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5d6-114">-DefaultProfile</span></span>
<span data-ttu-id="df5d6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df5d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df5d6-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df5d6-116">-InputObject</span></span>
<span data-ttu-id="df5d6-117">Объект input.</span><span class="sxs-lookup"><span data-stu-id="df5d6-117">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df5d6-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df5d6-118">-Name</span></span>
<span data-ttu-id="df5d6-119">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="df5d6-119">Resource name.</span></span>

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

### <span data-ttu-id="df5d6-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df5d6-120">-PassThru</span></span>
<span data-ttu-id="df5d6-121">Возвращает значение, указывающее, была ли операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="df5d6-121">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="df5d6-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df5d6-122">-ResourceId</span></span>
<span data-ttu-id="df5d6-123">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="df5d6-123">Resource ID.</span></span>

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

### <span data-ttu-id="df5d6-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df5d6-124">-Confirm</span></span>
<span data-ttu-id="df5d6-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df5d6-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df5d6-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df5d6-126">-WhatIf</span></span>
<span data-ttu-id="df5d6-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df5d6-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df5d6-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df5d6-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df5d6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5d6-129">CommonParameters</span></span>
<span data-ttu-id="df5d6-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df5d6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5d6-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df5d6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5d6-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df5d6-132">INPUTS</span></span>

### <span data-ttu-id="df5d6-133">System. String</span><span class="sxs-lookup"><span data-stu-id="df5d6-133">System.String</span></span>

### <span data-ttu-id="df5d6-134">Microsoft. Azure. Commands. Security. Models. SecurityContacts. PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="df5d6-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="df5d6-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df5d6-135">OUTPUTS</span></span>

### <span data-ttu-id="df5d6-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="df5d6-136">System.Boolean</span></span>

## <span data-ttu-id="df5d6-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="df5d6-137">NOTES</span></span>

## <span data-ttu-id="df5d6-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df5d6-138">RELATED LINKS</span></span>
