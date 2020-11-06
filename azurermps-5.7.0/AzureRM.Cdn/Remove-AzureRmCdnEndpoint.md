---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/remove-azurermcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Remove-AzureRmCdnEndpoint.md
ms.openlocfilehash: 8748806346baa4f84550d15749e7792ae928ad34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563735"
---
# <span data-ttu-id="5ecad-101">Remove-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-101">Remove-AzureRmCdnEndpoint</span></span>

## <span data-ttu-id="5ecad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5ecad-102">SYNOPSIS</span></span>
<span data-ttu-id="5ecad-103">Удаляет конечную точку CDN.</span><span class="sxs-lookup"><span data-stu-id="5ecad-103">Removes a CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ecad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5ecad-104">SYNTAX</span></span>

### <span data-ttu-id="5ecad-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ecad-105">ByFieldsParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ecad-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ecad-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ecad-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ecad-107">DESCRIPTION</span></span>
<span data-ttu-id="5ecad-108">Командлет **Remove-AzureRmCdnEndpoint** удаляет конечную точку сети доставки содержимого (CDN) для Azure.</span><span class="sxs-lookup"><span data-stu-id="5ecad-108">The **Remove-AzureRmCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="5ecad-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5ecad-109">EXAMPLES</span></span>

## <span data-ttu-id="5ecad-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5ecad-110">PARAMETERS</span></span>

### <span data-ttu-id="5ecad-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-111">-CdnEndpoint</span></span>
<span data-ttu-id="5ecad-112">Указывает конечную точку, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ecad-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ecad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ecad-113">-DefaultProfile</span></span>
<span data-ttu-id="5ecad-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5ecad-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ecad-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5ecad-115">-EndpointName</span></span>
<span data-ttu-id="5ecad-116">Указывает имя конечной точки, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5ecad-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ecad-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ecad-117">-Force</span></span>
<span data-ttu-id="5ecad-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5ecad-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ecad-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ecad-119">-PassThru</span></span>
<span data-ttu-id="5ecad-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5ecad-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ecad-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5ecad-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ecad-122">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="5ecad-122">-ProfileName</span></span>
<span data-ttu-id="5ecad-123">Указывает имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5ecad-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5ecad-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ecad-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ecad-125">Указывает имя группы ресурсов, к которой принадлежит конечная точка.</span><span class="sxs-lookup"><span data-stu-id="5ecad-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="5ecad-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ecad-126">-Confirm</span></span>
<span data-ttu-id="5ecad-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5ecad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ecad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ecad-128">-WhatIf</span></span>
<span data-ttu-id="5ecad-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5ecad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ecad-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5ecad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ecad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ecad-131">CommonParameters</span></span>
<span data-ttu-id="5ecad-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5ecad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ecad-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ecad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ecad-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5ecad-134">INPUTS</span></span>

### <span data-ttu-id="5ecad-135">PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-135">PSEndpoint</span></span>
<span data-ttu-id="5ecad-136">Параметр "CdnEndpoint" принимает значение типа "PSEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5ecad-136">Parameter 'CdnEndpoint' accepts value of type 'PSEndpoint' from the pipeline</span></span>

## <span data-ttu-id="5ecad-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ecad-137">OUTPUTS</span></span>

### <span data-ttu-id="5ecad-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5ecad-138">System.Boolean</span></span>

## <span data-ttu-id="5ecad-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5ecad-139">NOTES</span></span>

## <span data-ttu-id="5ecad-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ecad-140">RELATED LINKS</span></span>

[<span data-ttu-id="5ecad-141">Get-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-141">Get-AzureRmCdnEndpoint</span></span>](./Get-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ecad-142">New-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-142">New-AzureRmCdnEndpoint</span></span>](./New-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ecad-143">Set-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-143">Set-AzureRmCdnEndpoint</span></span>](./Set-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ecad-144">Start-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-144">Start-AzureRmCdnEndpoint</span></span>](./Start-AzureRmCdnEndpoint.md)

[<span data-ttu-id="5ecad-145">Остановить-AzureRmCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="5ecad-145">Stop-AzureRmCdnEndpoint</span></span>](./Stop-AzureRmCdnEndpoint.md)


