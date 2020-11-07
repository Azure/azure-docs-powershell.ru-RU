---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: ba7bda62d0d001f11ff729ca0ecce6327b659855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730235"
---
# <span data-ttu-id="66c43-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66c43-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="66c43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="66c43-102">SYNOPSIS</span></span>
<span data-ttu-id="66c43-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="66c43-103">Removes an application gateway.</span></span>

## <span data-ttu-id="66c43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="66c43-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66c43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="66c43-105">DESCRIPTION</span></span>
<span data-ttu-id="66c43-106">Командлет **Remove-AzApplicationGateway** удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="66c43-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="66c43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="66c43-107">EXAMPLES</span></span>

### <span data-ttu-id="66c43-108">Пример 1: Удаление указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="66c43-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="66c43-109">Эта команда удаляет шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="66c43-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="66c43-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="66c43-110">PARAMETERS</span></span>

### <span data-ttu-id="66c43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c43-111">-DefaultProfile</span></span>
<span data-ttu-id="66c43-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="66c43-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66c43-113">-Force</span><span class="sxs-lookup"><span data-stu-id="66c43-113">-Force</span></span>
<span data-ttu-id="66c43-114">Указывает на то, что командлет принудительно приводит к удалению шлюза приложения независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="66c43-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="66c43-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="66c43-115">-Name</span></span>
<span data-ttu-id="66c43-116">Указывает имя удаляемого шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="66c43-116">Specifies the name of the application gateway to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c43-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66c43-117">-PassThru</span></span>
<span data-ttu-id="66c43-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="66c43-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="66c43-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="66c43-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="66c43-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66c43-120">-ResourceGroupName</span></span>
<span data-ttu-id="66c43-121">Указывает имя группы ресурсов, к которой принадлежит шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="66c43-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66c43-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66c43-122">-Confirm</span></span>
<span data-ttu-id="66c43-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="66c43-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66c43-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66c43-124">-WhatIf</span></span>
<span data-ttu-id="66c43-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="66c43-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66c43-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="66c43-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66c43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c43-127">CommonParameters</span></span>
<span data-ttu-id="66c43-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="66c43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c43-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66c43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c43-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="66c43-130">INPUTS</span></span>

### <span data-ttu-id="66c43-131">System. String</span><span class="sxs-lookup"><span data-stu-id="66c43-131">System.String</span></span>

### <span data-ttu-id="66c43-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66c43-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66c43-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="66c43-133">OUTPUTS</span></span>

### <span data-ttu-id="66c43-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="66c43-134">System.Boolean</span></span>

## <span data-ttu-id="66c43-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="66c43-135">NOTES</span></span>

## <span data-ttu-id="66c43-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="66c43-136">RELATED LINKS</span></span>

[<span data-ttu-id="66c43-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66c43-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


