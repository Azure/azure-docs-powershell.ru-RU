---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: aa8c40d7fb9f5ccb99ccdd88d6c04ceb4a888bf2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401215"
---
# <span data-ttu-id="3750b-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3750b-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="3750b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3750b-102">SYNOPSIS</span></span>
<span data-ttu-id="3750b-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="3750b-103">Removes an application gateway.</span></span>

## <span data-ttu-id="3750b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3750b-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3750b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3750b-105">DESCRIPTION</span></span>
<span data-ttu-id="3750b-106">Для **удаления шлюза приложения удаляется cmdlet Remove-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="3750b-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="3750b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3750b-107">EXAMPLES</span></span>

### <span data-ttu-id="3750b-108">Пример 1. Удаление указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="3750b-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3750b-109">Эта команда удаляет шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="3750b-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="3750b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3750b-110">PARAMETERS</span></span>

### <span data-ttu-id="3750b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3750b-111">-DefaultProfile</span></span>
<span data-ttu-id="3750b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3750b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3750b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="3750b-113">-Force</span></span>
<span data-ttu-id="3750b-114">Указывает на то, что при этом будет удален шлюз приложения независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="3750b-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="3750b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3750b-115">-Name</span></span>
<span data-ttu-id="3750b-116">Указывает имя удаляемого шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3750b-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="3750b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3750b-117">-PassThru</span></span>
<span data-ttu-id="3750b-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3750b-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3750b-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3750b-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3750b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3750b-120">-ResourceGroupName</span></span>
<span data-ttu-id="3750b-121">Имя группы ресурсов, к которой принадлежит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="3750b-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="3750b-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3750b-122">-Confirm</span></span>
<span data-ttu-id="3750b-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3750b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3750b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3750b-124">-WhatIf</span></span>
<span data-ttu-id="3750b-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3750b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3750b-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3750b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3750b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3750b-127">CommonParameters</span></span>
<span data-ttu-id="3750b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3750b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3750b-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3750b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3750b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3750b-130">INPUTS</span></span>

### <span data-ttu-id="3750b-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3750b-131">System.String</span></span>

### <span data-ttu-id="3750b-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3750b-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3750b-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3750b-133">OUTPUTS</span></span>

### <span data-ttu-id="3750b-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3750b-134">System.Boolean</span></span>

## <span data-ttu-id="3750b-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3750b-135">NOTES</span></span>

## <span data-ttu-id="3750b-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3750b-136">RELATED LINKS</span></span>

[<span data-ttu-id="3750b-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3750b-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


