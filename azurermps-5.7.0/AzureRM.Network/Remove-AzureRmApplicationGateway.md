---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGateway.md
ms.openlocfilehash: b743c9b2fa0e8abff1a878b6cdb780c025300ba7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559003"
---
# <span data-ttu-id="a46a5-101">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a46a5-101">Remove-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="a46a5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a46a5-102">SYNOPSIS</span></span>
<span data-ttu-id="a46a5-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a46a5-103">Removes an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a46a5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a46a5-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a46a5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a46a5-105">DESCRIPTION</span></span>
<span data-ttu-id="a46a5-106">Командлет **Remove-AzureRmApplicationGateway** удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a46a5-106">The **Remove-AzureRmApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="a46a5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a46a5-107">EXAMPLES</span></span>

### <span data-ttu-id="a46a5-108">Пример 1: Удаление указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="a46a5-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a46a5-109">Эта команда удаляет шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a46a5-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a46a5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a46a5-110">PARAMETERS</span></span>

### <span data-ttu-id="a46a5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a46a5-111">-DefaultProfile</span></span>
<span data-ttu-id="a46a5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a46a5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a46a5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a46a5-113">-Force</span></span>
<span data-ttu-id="a46a5-114">Указывает на то, что командлет принудительно приводит к удалению шлюза приложения независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a46a5-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="a46a5-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a46a5-115">-Name</span></span>
<span data-ttu-id="a46a5-116">Указывает имя удаляемого шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a46a5-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a46a5-117">-PassThru</span></span>
<span data-ttu-id="a46a5-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a46a5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a46a5-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a46a5-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a46a5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a46a5-120">-ResourceGroupName</span></span>
<span data-ttu-id="a46a5-121">Указывает имя группы ресурсов, к которой принадлежит шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="a46a5-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a46a5-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a46a5-122">-Confirm</span></span>
<span data-ttu-id="a46a5-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a46a5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a46a5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a46a5-124">-WhatIf</span></span>
<span data-ttu-id="a46a5-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a46a5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a46a5-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a46a5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a46a5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a46a5-127">CommonParameters</span></span>
<span data-ttu-id="a46a5-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a46a5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a46a5-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a46a5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a46a5-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a46a5-130">INPUTS</span></span>

### <span data-ttu-id="a46a5-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="a46a5-131">None</span></span>
<span data-ttu-id="a46a5-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a46a5-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a46a5-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a46a5-133">OUTPUTS</span></span>

### <span data-ttu-id="a46a5-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a46a5-134">System.String</span></span>

## <span data-ttu-id="a46a5-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="a46a5-135">NOTES</span></span>

## <span data-ttu-id="a46a5-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a46a5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a46a5-137">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a46a5-137">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)


