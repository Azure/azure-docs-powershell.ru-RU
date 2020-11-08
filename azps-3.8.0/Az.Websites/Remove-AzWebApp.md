---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065197"
---
# <span data-ttu-id="333b7-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="333b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="333b7-102">SYNOPSIS</span></span>
<span data-ttu-id="333b7-103">Удаление веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="333b7-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="333b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="333b7-104">SYNTAX</span></span>

### <span data-ttu-id="333b7-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="333b7-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="333b7-106">S2</span><span class="sxs-lookup"><span data-stu-id="333b7-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="333b7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="333b7-107">DESCRIPTION</span></span>
<span data-ttu-id="333b7-108">Командлет **Remove-AzWebApp** удаляет веб-приложение Azure, которое предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="333b7-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="333b7-109">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="333b7-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="333b7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="333b7-110">EXAMPLES</span></span>

### <span data-ttu-id="333b7-111">Пример 1: удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="333b7-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="333b7-112">Эта команда удаляет веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="333b7-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="333b7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="333b7-113">PARAMETERS</span></span>

### <span data-ttu-id="333b7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="333b7-114">-AsJob</span></span>
<span data-ttu-id="333b7-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="333b7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="333b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b7-116">-DefaultProfile</span></span>
<span data-ttu-id="333b7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="333b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="333b7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="333b7-118">-Force</span></span>
<span data-ttu-id="333b7-119">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="333b7-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="333b7-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="333b7-120">-Name</span></span>
<span data-ttu-id="333b7-121">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-121">WebApp Name</span></span>

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

### <span data-ttu-id="333b7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333b7-122">-ResourceGroupName</span></span>
<span data-ttu-id="333b7-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="333b7-123">Resource Group Name</span></span>

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

### <span data-ttu-id="333b7-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-124">-WebApp</span></span>
<span data-ttu-id="333b7-125">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-125">WebApp Object</span></span>

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

### <span data-ttu-id="333b7-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="333b7-126">-Confirm</span></span>
<span data-ttu-id="333b7-127">Запрашивает подтверждение перед запуском командлета. Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="333b7-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333b7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333b7-128">-WhatIf</span></span>
<span data-ttu-id="333b7-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="333b7-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333b7-130">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="333b7-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333b7-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="333b7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b7-132">CommonParameters</span></span>
<span data-ttu-id="333b7-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="333b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b7-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="333b7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b7-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="333b7-135">INPUTS</span></span>

### <span data-ttu-id="333b7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="333b7-136">System.String</span></span>

### <span data-ttu-id="333b7-137">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="333b7-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="333b7-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="333b7-138">OUTPUTS</span></span>

### <span data-ttu-id="333b7-139">System. void</span><span class="sxs-lookup"><span data-stu-id="333b7-139">System.Void</span></span>

## <span data-ttu-id="333b7-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="333b7-140">NOTES</span></span>

## <span data-ttu-id="333b7-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="333b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="333b7-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="333b7-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="333b7-144">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="333b7-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="333b7-146">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="333b7-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


