---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/stop-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Stop-AzureRmCdnEndpoint.md
ms.openlocfilehash: 508465250489f2bcd0b031627258f11370fccfa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559228"
---
# <span data-ttu-id="f00d2-101">Stop-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-101">Stop-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="f00d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f00d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f00d2-103">Останавливает конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="f00d2-103">Stops the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f00d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f00d2-104">SYNTAX</span></span>

### <span data-ttu-id="f00d2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f00d2-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f00d2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f00d2-106">ByObjectParameterSet</span></span>
```
Stop-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f00d2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00d2-107">DESCRIPTION</span></span>
<span data-ttu-id="f00d2-108">Командлет **Stop-AzureRmCdnEndpoint** останавливает конечную точку сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="f00d2-108">The **Stop-AzureRmCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f00d2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f00d2-109">EXAMPLES</span></span>

## <span data-ttu-id="f00d2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f00d2-110">PARAMETERS</span></span>

### <span data-ttu-id="f00d2-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-111">-CdnEndpoint</span></span>
<span data-ttu-id="f00d2-112">Указывает объект конечной точки, который останавливается для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="f00d2-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00d2-113">-DefaultProfile</span></span>
<span data-ttu-id="f00d2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f00d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f00d2-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f00d2-115">-EndpointName</span></span>
<span data-ttu-id="f00d2-116">Указывает имя конечной точки, которую завершает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f00d2-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f00d2-117">-PassThru</span></span>
<span data-ttu-id="f00d2-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f00d2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f00d2-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f00d2-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="f00d2-120">-ProfileName</span></span>
<span data-ttu-id="f00d2-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f00d2-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f00d2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f00d2-123">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f00d2-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f00d2-124">-Confirm</span></span>
<span data-ttu-id="f00d2-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f00d2-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f00d2-126">-WhatIf</span></span>
<span data-ttu-id="f00d2-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f00d2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f00d2-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f00d2-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f00d2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00d2-129">CommonParameters</span></span>
<span data-ttu-id="f00d2-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f00d2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00d2-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f00d2-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00d2-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f00d2-132">INPUTS</span></span>

### <span data-ttu-id="f00d2-133">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-133">PSEndpoint</span></span>
<span data-ttu-id="f00d2-134">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f00d2-134">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f00d2-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f00d2-135">OUTPUTS</span></span>

### <span data-ttu-id="f00d2-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f00d2-136">System.Boolean</span></span>

## <span data-ttu-id="f00d2-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="f00d2-137">NOTES</span></span>

## <span data-ttu-id="f00d2-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f00d2-138">RELATED LINKS</span></span>

[<span data-ttu-id="f00d2-139">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-139">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f00d2-140">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-140">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f00d2-141">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-141">Remove-AzureRmCdnEndpoint</span></span>](./Remove-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f00d2-142">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-142">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="f00d2-143">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f00d2-143">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)


