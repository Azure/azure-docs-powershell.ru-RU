---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 3A4F8442-1268-44BC-91ED-47C03CD20C47
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnProfile.md
ms.openlocfilehash: ba45ea8d4c1b58290623f7f415f09cdb7663f575
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509345"
---
# <span data-ttu-id="f5656-101">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-101">Remove-AzCdnProfile</span></span>

## <span data-ttu-id="f5656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5656-102">SYNOPSIS</span></span>
<span data-ttu-id="f5656-103">Удаление профиля CDN.</span><span class="sxs-lookup"><span data-stu-id="f5656-103">Removes a CDN profile.</span></span>

## <span data-ttu-id="f5656-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5656-104">SYNTAX</span></span>

### <span data-ttu-id="f5656-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5656-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnProfile -ProfileName <String> -ResourceGroupName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5656-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f5656-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnProfile -CdnProfile <PSProfile> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5656-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5656-107">DESCRIPTION</span></span>
<span data-ttu-id="f5656-108">С **его использованием** удаляется профиль сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="f5656-108">The **Remove-AzCdnProfile** cmdlet removes a Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="f5656-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5656-109">EXAMPLES</span></span>

## <span data-ttu-id="f5656-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5656-110">PARAMETERS</span></span>

### <span data-ttu-id="f5656-111">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-111">-CdnProfile</span></span>
<span data-ttu-id="f5656-112">Определяет профиль, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5656-112">Specifies the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f5656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-113">-DefaultProfile</span></span>
<span data-ttu-id="f5656-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5656-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5656-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f5656-115">-Force</span></span>
<span data-ttu-id="f5656-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f5656-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5656-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5656-117">-PassThru</span></span>
<span data-ttu-id="f5656-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f5656-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5656-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f5656-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5656-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f5656-120">-ProfileName</span></span>
<span data-ttu-id="f5656-121">Указывает имя профиля, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5656-121">Specifies the name of the profile that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f5656-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5656-122">-ResourceGroupName</span></span>
<span data-ttu-id="f5656-123">Имя группы ресурсов, к которой принадлежит профиль.</span><span class="sxs-lookup"><span data-stu-id="f5656-123">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="f5656-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5656-124">-Confirm</span></span>
<span data-ttu-id="f5656-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5656-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5656-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5656-126">-WhatIf</span></span>
<span data-ttu-id="f5656-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5656-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5656-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5656-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5656-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5656-129">CommonParameters</span></span>
<span data-ttu-id="f5656-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5656-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5656-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5656-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5656-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5656-132">INPUTS</span></span>

### <span data-ttu-id="f5656-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-133">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

### <span data-ttu-id="f5656-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f5656-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f5656-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5656-135">OUTPUTS</span></span>

### <span data-ttu-id="f5656-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f5656-136">System.Boolean</span></span>

## <span data-ttu-id="f5656-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5656-137">NOTES</span></span>

## <span data-ttu-id="f5656-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5656-138">RELATED LINKS</span></span>

[<span data-ttu-id="f5656-139">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-139">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="f5656-140">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-140">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="f5656-141">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f5656-141">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


