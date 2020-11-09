---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319199"
---
# <span data-ttu-id="f9b8b-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9b8b-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="f9b8b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9b8b-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b8b-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-103">Removes an application gateway.</span></span>

## <span data-ttu-id="f9b8b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9b8b-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9b8b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9b8b-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b8b-106">Командлет **Remove-AzApplicationGateway** удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="f9b8b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9b8b-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b8b-108">Пример 1: Удаление указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="f9b8b-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f9b8b-109">Эта команда удаляет шлюз приложения с именем ApplicationGateway01 в группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="f9b8b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9b8b-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b8b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b8b-111">-DefaultProfile</span></span>
<span data-ttu-id="f9b8b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9b8b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f9b8b-113">-Force</span></span>
<span data-ttu-id="f9b8b-114">Указывает на то, что командлет принудительно приводит к удалению шлюза приложения независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="f9b8b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9b8b-115">-Name</span></span>
<span data-ttu-id="f9b8b-116">Указывает имя удаляемого шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="f9b8b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9b8b-117">-PassThru</span></span>
<span data-ttu-id="f9b8b-118">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f9b8b-119">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f9b8b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9b8b-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9b8b-121">Указывает имя группы ресурсов, к которой принадлежит шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="f9b8b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9b8b-122">-Confirm</span></span>
<span data-ttu-id="f9b8b-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9b8b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9b8b-124">-WhatIf</span></span>
<span data-ttu-id="f9b8b-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9b8b-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9b8b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b8b-127">CommonParameters</span></span>
<span data-ttu-id="f9b8b-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9b8b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b8b-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9b8b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b8b-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9b8b-130">INPUTS</span></span>

### <span data-ttu-id="f9b8b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f9b8b-131">System.String</span></span>

### <span data-ttu-id="f9b8b-132">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9b8b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9b8b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9b8b-133">OUTPUTS</span></span>

### <span data-ttu-id="f9b8b-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9b8b-134">System.Boolean</span></span>

## <span data-ttu-id="f9b8b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9b8b-135">NOTES</span></span>

## <span data-ttu-id="f9b8b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9b8b-136">RELATED LINKS</span></span>

[<span data-ttu-id="f9b8b-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f9b8b-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


