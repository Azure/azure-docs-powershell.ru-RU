---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/remove-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b06a5253ac5b26097d2dc4dea9c3d557c00a4d46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558115"
---
# <span data-ttu-id="52aeb-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="52aeb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52aeb-102">SYNOPSIS</span></span>
<span data-ttu-id="52aeb-103">Удаление веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="52aeb-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52aeb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52aeb-104">SYNTAX</span></span>

### <span data-ttu-id="52aeb-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="52aeb-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52aeb-106">S2</span><span class="sxs-lookup"><span data-stu-id="52aeb-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52aeb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52aeb-107">DESCRIPTION</span></span>
<span data-ttu-id="52aeb-108">Командлет **Remove-AzureRmWebApp** удаляет веб-приложение Azure, которое предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="52aeb-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="52aeb-109">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="52aeb-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="52aeb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52aeb-110">EXAMPLES</span></span>

### <span data-ttu-id="52aeb-111">Пример 1: удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="52aeb-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="52aeb-112">Эта команда удаляет веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="52aeb-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="52aeb-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52aeb-113">PARAMETERS</span></span>

### <span data-ttu-id="52aeb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52aeb-114">-AsJob</span></span>
<span data-ttu-id="52aeb-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="52aeb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52aeb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52aeb-116">-DefaultProfile</span></span>
<span data-ttu-id="52aeb-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52aeb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52aeb-118">-Force</span><span class="sxs-lookup"><span data-stu-id="52aeb-118">-Force</span></span>
<span data-ttu-id="52aeb-119">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="52aeb-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="52aeb-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="52aeb-120">-Name</span></span>
<span data-ttu-id="52aeb-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-121">WebApp Name</span></span>

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

### <span data-ttu-id="52aeb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52aeb-122">-ResourceGroupName</span></span>
<span data-ttu-id="52aeb-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="52aeb-123">Resource Group Name</span></span>

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

### <span data-ttu-id="52aeb-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-124">-WebApp</span></span>
<span data-ttu-id="52aeb-125">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-125">WebApp Object</span></span>

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

### <span data-ttu-id="52aeb-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52aeb-126">-Confirm</span></span>
<span data-ttu-id="52aeb-127">Запрашивает подтверждение перед запуском командлета. Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52aeb-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52aeb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52aeb-128">-WhatIf</span></span>
<span data-ttu-id="52aeb-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52aeb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52aeb-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52aeb-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52aeb-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52aeb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52aeb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52aeb-132">CommonParameters</span></span>
<span data-ttu-id="52aeb-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52aeb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52aeb-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52aeb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52aeb-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52aeb-135">INPUTS</span></span>

### <span data-ttu-id="52aeb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="52aeb-136">System.String</span></span>

### <span data-ttu-id="52aeb-137">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="52aeb-137">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="52aeb-138">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="52aeb-138">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="52aeb-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52aeb-139">OUTPUTS</span></span>

### <span data-ttu-id="52aeb-140">System. void</span><span class="sxs-lookup"><span data-stu-id="52aeb-140">System.Void</span></span>

## <span data-ttu-id="52aeb-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="52aeb-141">NOTES</span></span>

## <span data-ttu-id="52aeb-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52aeb-142">RELATED LINKS</span></span>

[<span data-ttu-id="52aeb-143">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-143">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="52aeb-144">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-144">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="52aeb-145">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-145">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="52aeb-146">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-146">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="52aeb-147">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="52aeb-147">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


