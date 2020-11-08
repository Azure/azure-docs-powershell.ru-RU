---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074084"
---
# <span data-ttu-id="3d43d-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d43d-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="3d43d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3d43d-102">SYNOPSIS</span></span>
<span data-ttu-id="3d43d-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="3d43d-103">Removes an application security group.</span></span>

## <span data-ttu-id="3d43d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3d43d-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d43d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d43d-105">DESCRIPTION</span></span>
<span data-ttu-id="3d43d-106">Командлет **Remove-AzApplicationSecurityGroup** удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="3d43d-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="3d43d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3d43d-107">EXAMPLES</span></span>

### <span data-ttu-id="3d43d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3d43d-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="3d43d-109">Эта команда удаляет группу безопасности приложений с именем MyApplicationSecurityGrouo в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3d43d-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="3d43d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3d43d-110">PARAMETERS</span></span>

### <span data-ttu-id="3d43d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d43d-111">-AsJob</span></span>
<span data-ttu-id="3d43d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3d43d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d43d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d43d-113">-DefaultProfile</span></span>
<span data-ttu-id="3d43d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3d43d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d43d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3d43d-115">-Force</span></span>
<span data-ttu-id="3d43d-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="3d43d-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="3d43d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3d43d-117">-Name</span></span>
<span data-ttu-id="3d43d-118">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="3d43d-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="3d43d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d43d-119">-PassThru</span></span>
<span data-ttu-id="3d43d-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="3d43d-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3d43d-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="3d43d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3d43d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d43d-122">-ResourceGroupName</span></span>
<span data-ttu-id="3d43d-123">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="3d43d-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="3d43d-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d43d-124">-Confirm</span></span>
<span data-ttu-id="3d43d-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3d43d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d43d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d43d-126">-WhatIf</span></span>
<span data-ttu-id="3d43d-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3d43d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d43d-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3d43d-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d43d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d43d-129">CommonParameters</span></span>
<span data-ttu-id="3d43d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3d43d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d43d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d43d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d43d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3d43d-132">INPUTS</span></span>

### <span data-ttu-id="3d43d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3d43d-133">System.String</span></span>

## <span data-ttu-id="3d43d-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d43d-134">OUTPUTS</span></span>

### <span data-ttu-id="3d43d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d43d-135">System.Boolean</span></span>

## <span data-ttu-id="3d43d-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3d43d-136">NOTES</span></span>

## <span data-ttu-id="3d43d-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d43d-137">RELATED LINKS</span></span>

[<span data-ttu-id="3d43d-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d43d-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="3d43d-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3d43d-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
