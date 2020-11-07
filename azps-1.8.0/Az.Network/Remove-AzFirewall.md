---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9DBD5ADF-C30E-4D1A-A4CB-4D70C21088F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewall.md
ms.openlocfilehash: b46540a614f25a3923301e28cd19d8f1b76af53c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730166"
---
# <span data-ttu-id="e04c1-101">Remove-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e04c1-101">Remove-AzFirewall</span></span>

## <span data-ttu-id="e04c1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e04c1-102">SYNOPSIS</span></span>
<span data-ttu-id="e04c1-103">Удаление брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e04c1-103">Remove a Firewall.</span></span>

## <span data-ttu-id="e04c1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e04c1-104">SYNTAX</span></span>

```
Remove-AzFirewall -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e04c1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e04c1-105">DESCRIPTION</span></span>
<span data-ttu-id="e04c1-106">Командлет **Remove-AzFirewall** удаляет брандмауэр Azure.</span><span class="sxs-lookup"><span data-stu-id="e04c1-106">The **Remove-AzFirewall** cmdlet removes an Azure Firewall.</span></span>

## <span data-ttu-id="e04c1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e04c1-107">EXAMPLES</span></span>

### <span data-ttu-id="e04c1-108">1: создание и удаление брандмауэра</span><span class="sxs-lookup"><span data-stu-id="e04c1-108">1: Create and delete a Firewall</span></span>
```
New-AzFirewall -Name "azFw" -ResourceGroupName "rgName" -Location centralus 

Remove-AzFirewall -Name "azFw" -ResourceGroupName "rgName"
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e04c1-109">В этом примере создается брандмауэр, а затем он удаляется.</span><span class="sxs-lookup"><span data-stu-id="e04c1-109">This example creates a Firewall and then deletes it.</span></span> <span data-ttu-id="e04c1-110">Чтобы отключить вывод запроса при удалении брандмауэра, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="e04c1-110">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

### <span data-ttu-id="e04c1-111">2: выделяйте брандмауэр и удалите брандмауэр</span><span class="sxs-lookup"><span data-stu-id="e04c1-111">2: Deallocate the Firewall, then delete the Firewall</span></span>
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
Remove-AzFirewall -ResourceGroupName rgName -Name azFw
Confirm
Are you sure you want to remove resource 'azFw'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="e04c1-112">В этом примере извлекается брандмауэр, выделяются брандмауэром, а затем удаляется брандмауэр.</span><span class="sxs-lookup"><span data-stu-id="e04c1-112">This example retrieves a Firewall, deallocates the firewall, and then deletes the firewall.</span></span> <span data-ttu-id="e04c1-113">Команда "освободить" удаляет запущенную службу, но сохраняет конфигурацию брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e04c1-113">The Deallocate command removes the running service but preserves the firewall's configuration.</span></span> <span data-ttu-id="e04c1-114">Если пользователь хочет снова запустить службу, необходимо вызвать метод выделения на брандмауэре.</span><span class="sxs-lookup"><span data-stu-id="e04c1-114">If user wants to start the service again, the Allocate method should be called on the firewall.</span></span>
<span data-ttu-id="e04c1-115">Чтобы отключить вывод запроса при удалении брандмауэра, используйте флаг-force.</span><span class="sxs-lookup"><span data-stu-id="e04c1-115">To suppress the prompt when deleting the Firewall, use the -Force flag.</span></span>

## <span data-ttu-id="e04c1-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e04c1-116">PARAMETERS</span></span>

### <span data-ttu-id="e04c1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e04c1-117">-AsJob</span></span>
<span data-ttu-id="e04c1-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e04c1-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e04c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e04c1-119">-DefaultProfile</span></span>
<span data-ttu-id="e04c1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e04c1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e04c1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e04c1-121">-Force</span></span>
<span data-ttu-id="e04c1-122">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e04c1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e04c1-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e04c1-123">-Name</span></span>
<span data-ttu-id="e04c1-124">Указывает имя брандмауэра, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e04c1-124">Specifies the name of the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e04c1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e04c1-125">-PassThru</span></span>
<span data-ttu-id="e04c1-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e04c1-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e04c1-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e04c1-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e04c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e04c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="e04c1-129">Указывает имя группы ресурсов, которая содержит брандмауэр, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="e04c1-129">Specifies the name of the resource group that contains the firewall that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e04c1-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e04c1-130">-Confirm</span></span>
<span data-ttu-id="e04c1-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e04c1-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e04c1-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e04c1-132">-WhatIf</span></span>
<span data-ttu-id="e04c1-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e04c1-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e04c1-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e04c1-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e04c1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e04c1-135">CommonParameters</span></span>
<span data-ttu-id="e04c1-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e04c1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e04c1-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e04c1-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e04c1-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e04c1-138">INPUTS</span></span>

### <span data-ttu-id="e04c1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e04c1-139">System.String</span></span>

## <span data-ttu-id="e04c1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e04c1-140">OUTPUTS</span></span>

### <span data-ttu-id="e04c1-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e04c1-141">System.Boolean</span></span>

## <span data-ttu-id="e04c1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e04c1-142">NOTES</span></span>

## <span data-ttu-id="e04c1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e04c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="e04c1-144">Get-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e04c1-144">Get-AzFirewall</span></span>](./Get-AzFirewall.md)

[<span data-ttu-id="e04c1-145">New-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e04c1-145">New-AzFirewall</span></span>](./New-AzFirewall.md)

[<span data-ttu-id="e04c1-146">Set-AzFirewall</span><span class="sxs-lookup"><span data-stu-id="e04c1-146">Set-AzFirewall</span></span>](./Set-AzFirewall.md)
