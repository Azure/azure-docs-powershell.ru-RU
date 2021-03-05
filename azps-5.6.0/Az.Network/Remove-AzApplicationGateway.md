---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E9390015-FD5C-4015-BA81-3445ADF8F8BF
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGateway.md
ms.openlocfilehash: 7095190570e649ab5262de0a8cebfc97d55fbf17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984296"
---
# <span data-ttu-id="a3dc2-101">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3dc2-101">Remove-AzApplicationGateway</span></span>

## <span data-ttu-id="a3dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="a3dc2-103">Удаляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-103">Removes an application gateway.</span></span>

## <span data-ttu-id="a3dc2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3dc2-104">SYNTAX</span></span>

```
Remove-AzApplicationGateway -Name <String> -ResourceGroupName <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3dc2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="a3dc2-106">Для **удаления шлюза приложения удаляется cmdlet Remove-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="a3dc2-106">The **Remove-AzApplicationGateway** cmdlet removes an application gateway.</span></span>

## <span data-ttu-id="a3dc2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3dc2-107">EXAMPLES</span></span>

### <span data-ttu-id="a3dc2-108">Пример 1. Удаление указанного шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="a3dc2-108">Example 1: Remove a specified application gateway</span></span>
```
PS C:\>Remove-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a3dc2-109">Эта команда удаляет шлюз приложения ApplicationGateway01 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-109">This command removes the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="a3dc2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3dc2-110">PARAMETERS</span></span>

### <span data-ttu-id="a3dc2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3dc2-111">-DefaultProfile</span></span>
<span data-ttu-id="a3dc2-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3dc2-113">-Force</span><span class="sxs-lookup"><span data-stu-id="a3dc2-113">-Force</span></span>
<span data-ttu-id="a3dc2-114">Указывает на то, что при этом будет удален шлюз приложения независимо от того, назначены ли ему ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-114">Indicates that the cmdlet forces the deletion of the application gateway regardless of whether resources are assigned to it.</span></span>

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

### <span data-ttu-id="a3dc2-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a3dc2-115">-Name</span></span>
<span data-ttu-id="a3dc2-116">Указывает имя удаляемого шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-116">Specifies the name of the application gateway to be removed.</span></span>

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

### <span data-ttu-id="a3dc2-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3dc2-117">-PassThru</span></span>
<span data-ttu-id="a3dc2-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3dc2-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3dc2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3dc2-120">-ResourceGroupName</span></span>
<span data-ttu-id="a3dc2-121">Имя группы ресурсов, к которой принадлежит шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-121">Specifies the name of the resource group name that the application gateway belongs to.</span></span>

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

### <span data-ttu-id="a3dc2-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3dc2-122">-Confirm</span></span>
<span data-ttu-id="a3dc2-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3dc2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3dc2-124">-WhatIf</span></span>
<span data-ttu-id="a3dc2-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3dc2-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3dc2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3dc2-127">CommonParameters</span></span>
<span data-ttu-id="a3dc2-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3dc2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3dc2-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3dc2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3dc2-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3dc2-130">INPUTS</span></span>

### <span data-ttu-id="a3dc2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a3dc2-131">System.String</span></span>

### <span data-ttu-id="a3dc2-132">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a3dc2-132">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a3dc2-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3dc2-133">OUTPUTS</span></span>

### <span data-ttu-id="a3dc2-134">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3dc2-134">System.Boolean</span></span>

## <span data-ttu-id="a3dc2-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3dc2-135">NOTES</span></span>

## <span data-ttu-id="a3dc2-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3dc2-136">RELATED LINKS</span></span>

[<span data-ttu-id="a3dc2-137">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3dc2-137">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)


