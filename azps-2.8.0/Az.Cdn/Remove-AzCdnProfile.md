---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: 6b8a5d9bd25c6f79cbfd70c509c9683b80453fe9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727573"
---
# <span data-ttu-id="aa0fe-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="aa0fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa0fe-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0fe-103">Удаление профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="aa0fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa0fe-104">SYNTAX</span></span>

### <span data-ttu-id="aa0fe-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa0fe-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0fe-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa0fe-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa0fe-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa0fe-107">DESCRIPTION</span></span>
<span data-ttu-id="aa0fe-108">Командлет **Remove-AzCdnProfile** удаляет профиль сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="aa0fe-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa0fe-109">EXAMPLES</span></span>

## <span data-ttu-id="aa0fe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa0fe-110">PARAMETERS</span></span>

### <span data-ttu-id="aa0fe-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-111">-CdnProfile</span></span>
<span data-ttu-id="aa0fe-112">Указывает профиль, который удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa0fe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-113">-DefaultProfile</span></span>
<span data-ttu-id="aa0fe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa0fe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa0fe-115">-Force</span><span class="sxs-lookup"><span data-stu-id="aa0fe-115">-Force</span></span>
<span data-ttu-id="aa0fe-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa0fe-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa0fe-117">-PassThru</span></span>
<span data-ttu-id="aa0fe-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa0fe-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa0fe-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="aa0fe-120">-ProfileName</span></span>
<span data-ttu-id="aa0fe-121">Указывает имя профиля, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aa0fe-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0fe-122">-ResourceGroupName</span></span>
<span data-ttu-id="aa0fe-123">Указывает имя группы ресурсов, к которой относится профиль.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="aa0fe-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa0fe-124">-Confirm</span></span>
<span data-ttu-id="aa0fe-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0fe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa0fe-126">-WhatIf</span></span>
<span data-ttu-id="aa0fe-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0fe-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa0fe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0fe-129">CommonParameters</span></span>
<span data-ttu-id="aa0fe-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa0fe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0fe-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa0fe-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0fe-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa0fe-132">INPUTS</span></span>

### <span data-ttu-id="aa0fe-133">Microsoft. Azure. Commands. CDN. Models. Profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="aa0fe-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="aa0fe-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="aa0fe-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa0fe-135">OUTPUTS</span></span>

### <span data-ttu-id="aa0fe-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="aa0fe-136">System.Boolean</span></span>

## <span data-ttu-id="aa0fe-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa0fe-137">NOTES</span></span>

## <span data-ttu-id="aa0fe-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa0fe-138">RELATED LINKS</span></span>

[<span data-ttu-id="aa0fe-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="aa0fe-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="aa0fe-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="aa0fe-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


