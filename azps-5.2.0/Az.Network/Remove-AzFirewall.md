---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401452"
---
# <span data-ttu-id="f6cb5-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f6cb5-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="f6cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cb5-103">Удаление брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-103">Remove a Firewall.</span></span>

## <span data-ttu-id="f6cb5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f6cb5-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6cb5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f6cb5-105">DESCRIPTION</span></span>
<span data-ttu-id="f6cb5-106">С **помощью cmdlet Remove-AzFirewall** удаляется брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="f6cb5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f6cb5-107">EXAMPLES</span></span>

### <span data-ttu-id="f6cb5-108">Пример 1. Создание и удаление брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f6cb5-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="f6cb5-109">В этом примере создается брандмауэр, а затем удаляется.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="f6cb5-110">Чтобы скрыть запрос при удалении брандмауэра, используйте флажок -Force.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="f6cb5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6cb5-111">PARAMETERS</span></span>

### <span data-ttu-id="f6cb5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6cb5-112">-AsJob</span></span>
<span data-ttu-id="f6cb5-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="f6cb5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6cb5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cb5-114">-DefaultProfile</span></span>
<span data-ttu-id="f6cb5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6cb5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="f6cb5-116">-Force</span></span>
<span data-ttu-id="f6cb5-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f6cb5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f6cb5-118">-Name</span></span>
<span data-ttu-id="f6cb5-119">Указывает имя брандмауэра, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6cb5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6cb5-120">-PassThru</span></span>
<span data-ttu-id="f6cb5-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6cb5-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6cb5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6cb5-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6cb5-124">Имя группы ресурсов, которая содержит брандмауэр, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f6cb5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6cb5-125">-Confirm</span></span>
<span data-ttu-id="f6cb5-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6cb5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6cb5-127">-WhatIf</span></span>
<span data-ttu-id="f6cb5-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6cb5-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6cb5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cb5-130">CommonParameters</span></span>
<span data-ttu-id="f6cb5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6cb5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cb5-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6cb5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cb5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f6cb5-133">INPUTS</span></span>

### <span data-ttu-id="f6cb5-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f6cb5-134">System.String</span></span>

## <span data-ttu-id="f6cb5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f6cb5-135">OUTPUTS</span></span>

### <span data-ttu-id="f6cb5-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6cb5-136">System.Boolean</span></span>

## <span data-ttu-id="f6cb5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f6cb5-137">NOTES</span></span>

## <span data-ttu-id="f6cb5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f6cb5-138">RELATED LINKS</span></span>

[<span data-ttu-id="f6cb5-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f6cb5-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="f6cb5-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f6cb5-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="f6cb5-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="f6cb5-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
