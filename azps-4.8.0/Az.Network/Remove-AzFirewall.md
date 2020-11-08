---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: 52d2907769ac59a9c71fccef6baf08cc4d13bae8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244087"
---
# <span data-ttu-id="dbd98-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dbd98-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="dbd98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dbd98-102">SYNOPSIS</span></span>
<span data-ttu-id="dbd98-103">Удаление брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="dbd98-103">Remove a Firewall.</span></span>

## <span data-ttu-id="dbd98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dbd98-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbd98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd98-105">DESCRIPTION</span></span>
<span data-ttu-id="dbd98-106">Командлет **Remove-AzFirewall** удаляет брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd98-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="dbd98-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dbd98-107">EXAMPLES</span></span>

### <span data-ttu-id="dbd98-108">Пример 1: создание и удаление брандмауэра</span><span class="sxs-lookup"><span data-stu-id="dbd98-108">Example 1: Create and delete a Firewall</span></span>
```powershell
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="dbd98-109">В этом примере создается брандмауэр, а затем он удаляется.</span><span class="sxs-lookup"><span data-stu-id="dbd98-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="dbd98-110">Чтобы отключить вывод запроса при удалении брандмауэра, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="dbd98-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="dbd98-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dbd98-111">PARAMETERS</span></span>

### <span data-ttu-id="dbd98-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbd98-112">-AsJob</span></span>
<span data-ttu-id="dbd98-113">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dbd98-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbd98-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbd98-114">-DefaultProfile</span></span>
<span data-ttu-id="dbd98-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbd98-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbd98-116">-Force</span><span class="sxs-lookup"><span data-stu-id="dbd98-116">-Force</span></span>
<span data-ttu-id="dbd98-117">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="dbd98-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="dbd98-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dbd98-118">-Name</span></span>
<span data-ttu-id="dbd98-119">Указывает имя брандмауэра, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dbd98-119">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbd98-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dbd98-120">-PassThru</span></span>
<span data-ttu-id="dbd98-121">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="dbd98-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dbd98-122">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="dbd98-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dbd98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbd98-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbd98-124">Указывает имя группы ресурсов, которая содержит брандмауэр, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="dbd98-124">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dbd98-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbd98-125">-Confirm</span></span>
<span data-ttu-id="dbd98-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dbd98-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbd98-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbd98-127">-WhatIf</span></span>
<span data-ttu-id="dbd98-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dbd98-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbd98-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dbd98-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbd98-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbd98-130">CommonParameters</span></span>
<span data-ttu-id="dbd98-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dbd98-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbd98-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbd98-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbd98-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dbd98-133">INPUTS</span></span>

### <span data-ttu-id="dbd98-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dbd98-134">System.String</span></span>

## <span data-ttu-id="dbd98-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbd98-135">OUTPUTS</span></span>

### <span data-ttu-id="dbd98-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dbd98-136">System.Boolean</span></span>

## <span data-ttu-id="dbd98-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="dbd98-137">NOTES</span></span>

## <span data-ttu-id="dbd98-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbd98-138">RELATED LINKS</span></span>

[<span data-ttu-id="dbd98-139">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dbd98-139">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="dbd98-140">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dbd98-140">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="dbd98-141">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="dbd98-141">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
