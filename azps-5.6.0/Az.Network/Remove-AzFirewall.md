---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 4be419ab76180174fd6132335822c361008ec872
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993779"
---
# <span data-ttu-id="7f917-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7f917-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="7f917-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f917-102">SYNOPSIS</span></span>
<span data-ttu-id="7f917-103">Удаление брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="7f917-103">Remove a Firewall.</span></span>

## <span data-ttu-id="7f917-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7f917-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f917-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f917-105">DESCRIPTION</span></span>
<span data-ttu-id="7f917-106">С **помощью cmdlet Remove-AzFirewall** удаляется брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="7f917-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="7f917-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7f917-107">EXAMPLES</span></span>

### <span data-ttu-id="7f917-108">Пример 1. Создание и удаление брандмауэра</span><span class="sxs-lookup"><span data-stu-id="7f917-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7f917-109">В этом примере создается брандмауэр, а затем удаляется.</span><span class="sxs-lookup"><span data-stu-id="7f917-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="7f917-110">Чтобы скрыть запрос при удалении брандмауэра, используйте флажок -Force.</span><span class="sxs-lookup"><span data-stu-id="7f917-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="7f917-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f917-111">PARAMETERS</span></span>

### <span data-ttu-id="7f917-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f917-112">-AsJob</span></span>
<span data-ttu-id="7f917-113">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7f917-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f917-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f917-114">-DefaultProfile</span></span>
<span data-ttu-id="7f917-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f917-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f917-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7f917-116">-Force</span></span>
<span data-ttu-id="7f917-117">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="7f917-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f917-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7f917-118">-Name</span></span>
<span data-ttu-id="7f917-119">Указывает имя брандмауэра, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f917-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f917-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f917-120">-PassThru</span></span>
<span data-ttu-id="7f917-121">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="7f917-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f917-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="7f917-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f917-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f917-123">-ResourceGroupName</span></span>
<span data-ttu-id="7f917-124">Имя группы ресурсов, которая содержит брандмауэр, который удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f917-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7f917-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f917-125">-Confirm</span></span>
<span data-ttu-id="7f917-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f917-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f917-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f917-127">-WhatIf</span></span>
<span data-ttu-id="7f917-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f917-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f917-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7f917-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f917-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f917-130">CommonParameters</span></span>
<span data-ttu-id="7f917-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f917-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f917-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f917-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f917-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7f917-133">INPUTS</span></span>

### <span data-ttu-id="7f917-134">System.String</span><span class="sxs-lookup"><span data-stu-id="7f917-134">System.String</span></span>

## <span data-ttu-id="7f917-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7f917-135">OUTPUTS</span></span>

### <span data-ttu-id="7f917-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7f917-136">System.Boolean</span></span>

## <span data-ttu-id="7f917-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7f917-137">NOTES</span></span>

## <span data-ttu-id="7f917-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f917-138">RELATED LINKS</span></span>

[<span data-ttu-id="7f917-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7f917-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="7f917-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7f917-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="7f917-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="7f917-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
