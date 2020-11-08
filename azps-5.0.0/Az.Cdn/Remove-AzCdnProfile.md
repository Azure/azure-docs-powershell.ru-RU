---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247650"
---
# <span data-ttu-id="b508e-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="b508e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b508e-102">SYNOPSIS</span></span>
<span data-ttu-id="b508e-103">Удаление профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="b508e-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="b508e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b508e-104">SYNTAX</span></span>

### <span data-ttu-id="b508e-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b508e-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b508e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b508e-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b508e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b508e-107">DESCRIPTION</span></span>
<span data-ttu-id="b508e-108">Командлет **Remove-AzCdnProfile** удаляет профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="b508e-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="b508e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b508e-109">EXAMPLES</span></span>

## <span data-ttu-id="b508e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b508e-110">PARAMETERS</span></span>

### <span data-ttu-id="b508e-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-111">-CdnProfile</span></span>
<span data-ttu-id="b508e-112">Указывает профиль, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b508e-112">Specifies the profile that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-113">-DefaultProfile</span></span>
<span data-ttu-id="b508e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b508e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b508e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b508e-115">-Force</span></span>
<span data-ttu-id="b508e-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b508e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b508e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b508e-117">-PassThru</span></span>
<span data-ttu-id="b508e-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b508e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b508e-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b508e-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="b508e-120">-ProfileName</span></span>
<span data-ttu-id="b508e-121">Указывает имя профиля, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b508e-121">Specifies the name of the profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b508e-122">-ResourceGroupName</span></span>
<span data-ttu-id="b508e-123">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="b508e-123">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b508e-124">-Confirm</span></span>
<span data-ttu-id="b508e-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b508e-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b508e-126">-WhatIf</span></span>
<span data-ttu-id="b508e-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b508e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b508e-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b508e-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b508e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b508e-129">CommonParameters</span></span>
<span data-ttu-id="b508e-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b508e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b508e-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b508e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b508e-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b508e-132">INPUTS</span></span>

### <span data-ttu-id="b508e-133">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="b508e-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b508e-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b508e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b508e-135">OUTPUTS</span></span>

### <span data-ttu-id="b508e-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b508e-136">System.Boolean</span></span>

## <span data-ttu-id="b508e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="b508e-137">NOTES</span></span>

## <span data-ttu-id="b508e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b508e-138">RELATED LINKS</span></span>

[<span data-ttu-id="b508e-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="b508e-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="b508e-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="b508e-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


