---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 49afefc7b80b5475735f61cb0511366b7f27a466
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570472"
---
# <span data-ttu-id="fbe7c-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="fbe7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbe7c-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe7c-103">Удаляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbe7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbe7c-104">SYNTAX</span></span>

### <span data-ttu-id="fbe7c-105">Наборы параметров для параметров полей</span><span class="sxs-lookup"><span data-stu-id="fbe7c-105">Parameter Set for fields parameters</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe7c-106">Параметр, заданный для параметров объекта</span><span class="sxs-lookup"><span data-stu-id="fbe7c-106">Parameter Set for object parameters</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbe7c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbe7c-107">DESCRIPTION</span></span>
<span data-ttu-id="fbe7c-108">Командлет **Remove-AzureRmCdnEndpoint** удаляет конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="fbe7c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbe7c-109">EXAMPLES</span></span>

## <span data-ttu-id="fbe7c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbe7c-110">PARAMETERS</span></span>

### <span data-ttu-id="fbe7c-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-111">-CdnEndpoint</span></span>
<span data-ttu-id="fbe7c-112">Указывает конечную точку, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-112">Specifies the endpoint that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe7c-113">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="fbe7c-113">-EndpointName</span></span>
<span data-ttu-id="fbe7c-114">Указывает имя конечной точки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-114">Specifies the name of the endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe7c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fbe7c-115">-Force</span></span>
<span data-ttu-id="fbe7c-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="fbe7c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbe7c-117">-PassThru</span></span>
<span data-ttu-id="fbe7c-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fbe7c-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fbe7c-120">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="fbe7c-120">-ProfileName</span></span>
<span data-ttu-id="fbe7c-121">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe7c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbe7c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fbe7c-123">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe7c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbe7c-124">-Confirm</span></span>
<span data-ttu-id="fbe7c-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe7c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe7c-126">-WhatIf</span></span>
<span data-ttu-id="fbe7c-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe7c-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe7c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe7c-129">-DefaultProfile</span></span>
<span data-ttu-id="fbe7c-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbe7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe7c-131">CommonParameters</span></span>
<span data-ttu-id="fbe7c-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe7c-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbe7c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe7c-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbe7c-134">INPUTS</span></span>

### <span data-ttu-id="fbe7c-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-135">PSEndpoint</span></span>
<span data-ttu-id="fbe7c-136">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fbe7c-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="fbe7c-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbe7c-137">OUTPUTS</span></span>

### <span data-ttu-id="fbe7c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fbe7c-138">System.Boolean</span></span>

## <span data-ttu-id="fbe7c-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbe7c-139">NOTES</span></span>

## <span data-ttu-id="fbe7c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbe7c-140">RELATED LINKS</span></span>

[<span data-ttu-id="fbe7c-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fbe7c-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fbe7c-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fbe7c-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="fbe7c-145">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="fbe7c-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


