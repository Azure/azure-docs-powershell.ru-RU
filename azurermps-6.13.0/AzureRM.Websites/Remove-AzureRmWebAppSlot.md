---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebAppSlot.md
ms.openlocfilehash: 7fdf5e8de2ec326888c57e8219a006f9ef447aa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565292"
---
# <span data-ttu-id="32b4b-101">Remove-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-101">Remove-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="32b4b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32b4b-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32b4b-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32b4b-103">SYNTAX</span></span>

### <span data-ttu-id="32b4b-104">Состояний</span><span class="sxs-lookup"><span data-stu-id="32b4b-104">S1</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32b4b-105">S2</span><span class="sxs-lookup"><span data-stu-id="32b4b-105">S2</span></span>
```
Remove-AzureRmWebAppSlot [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b4b-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b4b-106">DESCRIPTION</span></span>
<span data-ttu-id="32b4b-107">Командлет **Remove-AzureRmWebAppSlot** удаляет слот веб-приложения Azure, который предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="32b4b-107">The **Remove-AzureRmWebAppSlot** cmdlet removes an Azure Web App Slot provided the resource group and Web App name.</span></span>
<span data-ttu-id="32b4b-108">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="32b4b-108">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="32b4b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32b4b-109">EXAMPLES</span></span>

### <span data-ttu-id="32b4b-110">Пример 1: удаление слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="32b4b-110">Example 1: Remove a Web App Slot</span></span>
```
PS C:\>Remove-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite" -Slot "Slot001"
```

<span data-ttu-id="32b4b-111">Эта команда удаляет гнездо с именем Slot001, связанное с ContosoSite веб-приложения, которое принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="32b4b-111">This command removes the Slot named Slot001 associated with Web App ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="32b4b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32b4b-112">PARAMETERS</span></span>

### <span data-ttu-id="32b4b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32b4b-113">-AsJob</span></span>
<span data-ttu-id="32b4b-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="32b4b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32b4b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b4b-115">-DefaultProfile</span></span>
<span data-ttu-id="32b4b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32b4b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b4b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="32b4b-117">-Force</span></span>
<span data-ttu-id="32b4b-118">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="32b4b-118">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="32b4b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="32b4b-119">-Name</span></span>
<span data-ttu-id="32b4b-120">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="32b4b-120">WebApp Name</span></span>

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

### <span data-ttu-id="32b4b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b4b-121">-ResourceGroupName</span></span>
<span data-ttu-id="32b4b-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="32b4b-122">Resource Group Name</span></span>

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

### <span data-ttu-id="32b4b-123">-Slot</span><span class="sxs-lookup"><span data-stu-id="32b4b-123">-Slot</span></span>
<span data-ttu-id="32b4b-124">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="32b4b-124">WebApp Slot Name</span></span>

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

### <span data-ttu-id="32b4b-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="32b4b-125">-WebApp</span></span>
<span data-ttu-id="32b4b-126">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="32b4b-126">WebApp Object</span></span>

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

### <span data-ttu-id="32b4b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32b4b-127">-Confirm</span></span>
<span data-ttu-id="32b4b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="32b4b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b4b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b4b-129">-WhatIf</span></span>
<span data-ttu-id="32b4b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="32b4b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b4b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="32b4b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b4b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b4b-132">CommonParameters</span></span>
<span data-ttu-id="32b4b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32b4b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b4b-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b4b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b4b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32b4b-135">INPUTS</span></span>

### <span data-ttu-id="32b4b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="32b4b-136">System.String</span></span>

### <span data-ttu-id="32b4b-137">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="32b4b-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="32b4b-138">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32b4b-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="32b4b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32b4b-139">OUTPUTS</span></span>

### <span data-ttu-id="32b4b-140">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="32b4b-140">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="32b4b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="32b4b-141">NOTES</span></span>

## <span data-ttu-id="32b4b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32b4b-142">RELATED LINKS</span></span>

[<span data-ttu-id="32b4b-143">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-143">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-144">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-144">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-145">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-145">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-146">Set-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-146">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-147">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-147">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-148">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="32b4b-148">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="32b4b-149">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="32b4b-149">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
