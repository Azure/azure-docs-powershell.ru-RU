---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425252"
---
# <span data-ttu-id="d8f9c-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d8f9c-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="d8f9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-102">SYNOPSIS</span></span>
<span data-ttu-id="d8f9c-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-103">Removes an application security group.</span></span>

## <span data-ttu-id="d8f9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d8f9c-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8f9c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8f9c-105">DESCRIPTION</span></span>
<span data-ttu-id="d8f9c-106">Для удаления группы безопасности приложений удаляется ее cmdlet **Remove-AzApplicationSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="d8f9c-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="d8f9c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d8f9c-107">EXAMPLES</span></span>

### <span data-ttu-id="d8f9c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8f9c-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="d8f9c-109">Эта команда удаляет группу безопасности приложения MyApplicationSecurityGrouo в группе ресурсов MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="d8f9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-110">PARAMETERS</span></span>

### <span data-ttu-id="d8f9c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8f9c-111">-AsJob</span></span>
<span data-ttu-id="d8f9c-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8f9c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8f9c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8f9c-113">-DefaultProfile</span></span>
<span data-ttu-id="d8f9c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8f9c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d8f9c-115">-Force</span></span>
<span data-ttu-id="d8f9c-116">Не спрашивайте подтверждения, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="d8f9c-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="d8f9c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d8f9c-117">-Name</span></span>
<span data-ttu-id="d8f9c-118">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="d8f9c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8f9c-119">-PassThru</span></span>
<span data-ttu-id="d8f9c-120">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d8f9c-121">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d8f9c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8f9c-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8f9c-123">Имя группы ресурсов группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="d8f9c-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8f9c-124">-Confirm</span></span>
<span data-ttu-id="d8f9c-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8f9c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8f9c-126">-WhatIf</span></span>
<span data-ttu-id="d8f9c-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8f9c-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8f9c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8f9c-129">CommonParameters</span></span>
<span data-ttu-id="d8f9c-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8f9c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8f9c-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8f9c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8f9c-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-132">INPUTS</span></span>

### <span data-ttu-id="d8f9c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d8f9c-133">System.String</span></span>

## <span data-ttu-id="d8f9c-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8f9c-134">OUTPUTS</span></span>

### <span data-ttu-id="d8f9c-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8f9c-135">System.Boolean</span></span>

## <span data-ttu-id="d8f9c-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d8f9c-136">NOTES</span></span>

## <span data-ttu-id="d8f9c-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8f9c-137">RELATED LINKS</span></span>

[<span data-ttu-id="d8f9c-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d8f9c-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="d8f9c-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="d8f9c-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
