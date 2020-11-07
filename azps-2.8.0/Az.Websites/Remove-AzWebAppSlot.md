---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebAppSlot.md
ms.openlocfilehash: 38b11543140a0f789674e4109db8cc73c7843f02
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907062"
---
# <span data-ttu-id="dc85a-101">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-101">Remove-AzWebAppSlot</span></span>

## <span data-ttu-id="dc85a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dc85a-102">SYNOPSIS</span></span>

## <span data-ttu-id="dc85a-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dc85a-103">SYNTAX</span></span>

### <span data-ttu-id="dc85a-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="dc85a-104">S1</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc85a-105">S2</span><span class="sxs-lookup"><span data-stu-id="dc85a-105">S2</span></span>
```
Remove-AzWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc85a-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc85a-106">DESCRIPTION</span></span>
<span data-ttu-id="dc85a-107">Командлет **Remove-AzWebAppSlot** удаляет слот веб-приложения Azure, который предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="dc85a-107">The **Remove-AzWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="dc85a-108">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="dc85a-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="dc85a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dc85a-109">EXAMPLES</span></span>

### <span data-ttu-id="dc85a-110">Пример 1: удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="dc85a-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="dc85a-111">Эта команда удаляет гнездо с именем Slot001, связанное с ContosoSite веб-приложения, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="dc85a-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="dc85a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dc85a-112">PARAMETERS</span></span>

### <span data-ttu-id="dc85a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc85a-113">-AsJob</span></span>
<span data-ttu-id="dc85a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dc85a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc85a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc85a-115">-DefaultProfile</span></span>
<span data-ttu-id="dc85a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc85a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc85a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dc85a-117">-Force</span></span>
<span data-ttu-id="dc85a-118">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="dc85a-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="dc85a-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dc85a-119">-Name</span></span>
<span data-ttu-id="dc85a-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="dc85a-120">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc85a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc85a-121">-ResourceGroupName</span></span>
<span data-ttu-id="dc85a-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="dc85a-122">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85a-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="dc85a-123">-Slot</span></span>
<span data-ttu-id="dc85a-124">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="dc85a-124">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc85a-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="dc85a-125">-WebApp</span></span>
<span data-ttu-id="dc85a-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="dc85a-126">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc85a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc85a-127">-Confirm</span></span>
<span data-ttu-id="dc85a-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dc85a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc85a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc85a-129">-WhatIf</span></span>
<span data-ttu-id="dc85a-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dc85a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc85a-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dc85a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc85a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc85a-132">CommonParameters</span></span>
<span data-ttu-id="dc85a-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dc85a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc85a-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc85a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc85a-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dc85a-135">INPUTS</span></span>

### <span data-ttu-id="dc85a-136">System. String</span><span class="sxs-lookup"><span data-stu-id="dc85a-136">System.String</span></span>

### <span data-ttu-id="dc85a-137">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="dc85a-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="dc85a-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc85a-138">OUTPUTS</span></span>

### <span data-ttu-id="dc85a-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="dc85a-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="dc85a-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="dc85a-140">NOTES</span></span>

## <span data-ttu-id="dc85a-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc85a-141">RELATED LINKS</span></span>

[<span data-ttu-id="dc85a-142">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-142">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-143">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-143">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-144">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-144">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-145">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-145">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-146">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-146">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-147">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="dc85a-147">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="dc85a-148">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="dc85a-148">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
