---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationsecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationSecurityGroup.md
ms.openlocfilehash: 562a2fbf02bd6389b28543f09ace1c59b2e9ed1c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245961"
---
# <span data-ttu-id="35f19-101">Remove-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35f19-101">Remove-AzApplicationSecurityGroup</span></span>

## <span data-ttu-id="35f19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35f19-102">SYNOPSIS</span></span>
<span data-ttu-id="35f19-103">Удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="35f19-103">Removes an application security group.</span></span>

## <span data-ttu-id="35f19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35f19-104">SYNTAX</span></span>

```
Remove-AzApplicationSecurityGroup -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35f19-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f19-105">DESCRIPTION</span></span>
<span data-ttu-id="35f19-106">Командлет **Remove-AzApplicationSecurityGroup** удаляет группу безопасности приложений.</span><span class="sxs-lookup"><span data-stu-id="35f19-106">The **Remove-AzApplicationSecurityGroup** cmdlet removes an application security group.</span></span>

## <span data-ttu-id="35f19-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35f19-107">EXAMPLES</span></span>

### <span data-ttu-id="35f19-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35f19-108">Example 1</span></span>
```
PS C:\>Remove-AzApplicationSecurityGroup -Name "MyApplicationSecurityGrouo" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="35f19-109">Эта команда удаляет группу безопасности приложений с именем MyApplicationSecurityGrouo в группе ресурсов с именем MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="35f19-109">This command deletes an application security group named MyApplicationSecurityGrouo in the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="35f19-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35f19-110">PARAMETERS</span></span>

### <span data-ttu-id="35f19-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f19-111">-AsJob</span></span>
<span data-ttu-id="35f19-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="35f19-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="35f19-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f19-113">-DefaultProfile</span></span>
<span data-ttu-id="35f19-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35f19-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35f19-115">-Force</span><span class="sxs-lookup"><span data-stu-id="35f19-115">-Force</span></span>
<span data-ttu-id="35f19-116">Не запрашивать подтверждение, если вы хотите удалить ресурс</span><span class="sxs-lookup"><span data-stu-id="35f19-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="35f19-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35f19-117">-Name</span></span>
<span data-ttu-id="35f19-118">Имя группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="35f19-118">The name of the application security group.</span></span>

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

### <span data-ttu-id="35f19-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35f19-119">-PassThru</span></span>
<span data-ttu-id="35f19-120">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="35f19-120">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="35f19-121">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="35f19-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="35f19-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f19-122">-ResourceGroupName</span></span>
<span data-ttu-id="35f19-123">Имя группы ресурсов для группы безопасности приложения.</span><span class="sxs-lookup"><span data-stu-id="35f19-123">The resource group name of the application security group.</span></span>

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

### <span data-ttu-id="35f19-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35f19-124">-Confirm</span></span>
<span data-ttu-id="35f19-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35f19-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f19-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f19-126">-WhatIf</span></span>
<span data-ttu-id="35f19-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35f19-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f19-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35f19-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f19-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f19-129">CommonParameters</span></span>
<span data-ttu-id="35f19-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35f19-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f19-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35f19-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f19-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35f19-132">INPUTS</span></span>

### <span data-ttu-id="35f19-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35f19-133">System.String</span></span>

## <span data-ttu-id="35f19-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35f19-134">OUTPUTS</span></span>

### <span data-ttu-id="35f19-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35f19-135">System.Boolean</span></span>

## <span data-ttu-id="35f19-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="35f19-136">NOTES</span></span>

## <span data-ttu-id="35f19-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35f19-137">RELATED LINKS</span></span>

[<span data-ttu-id="35f19-138">New-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35f19-138">New-AzApplicationSecurityGroup</span></span>](./New-AzApplicationSecurityGroup.md)

[<span data-ttu-id="35f19-139">Get-AzApplicationSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="35f19-139">Get-AzApplicationSecurityGroup</span></span>](./Get-AzApplicationSecurityGroup.md)
