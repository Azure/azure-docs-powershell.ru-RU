---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/remove-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 64d463e6cbe3012b8d49e0a61b4f081f286e25b5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505756"
---
# <span data-ttu-id="1cbca-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="1cbca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cbca-102">SYNOPSIS</span></span>
<span data-ttu-id="1cbca-103">Удаляет Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1cbca-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="1cbca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1cbca-104">SYNTAX</span></span>

### <span data-ttu-id="1cbca-105">S1</span><span class="sxs-lookup"><span data-stu-id="1cbca-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cbca-106">S2</span><span class="sxs-lookup"><span data-stu-id="1cbca-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cbca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cbca-107">DESCRIPTION</span></span>
<span data-ttu-id="1cbca-108">С **помощью cmdlet Remove-AzWebApp** можно удалить azure Web App, при условии что группа ресурсов и имя веб-приложения были присвоены.</span><span class="sxs-lookup"><span data-stu-id="1cbca-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="1cbca-109">Этот cmdlet по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="1cbca-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="1cbca-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1cbca-110">EXAMPLES</span></span>

### <span data-ttu-id="1cbca-111">Пример 1. Удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1cbca-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="1cbca-112">Эта команда удаляет службу Azure Web App ContosoSite, которая принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="1cbca-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="1cbca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cbca-113">PARAMETERS</span></span>

### <span data-ttu-id="1cbca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1cbca-114">-AsJob</span></span>
<span data-ttu-id="1cbca-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1cbca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1cbca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cbca-116">-DefaultProfile</span></span>
<span data-ttu-id="1cbca-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cbca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cbca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1cbca-118">-Force</span></span>
<span data-ttu-id="1cbca-119">Параметр "Принудительно удалить"</span><span class="sxs-lookup"><span data-stu-id="1cbca-119">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="1cbca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1cbca-120">-Name</span></span>
<span data-ttu-id="1cbca-121">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="1cbca-121">WebApp Name</span></span>

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

### <span data-ttu-id="1cbca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cbca-122">-ResourceGroupName</span></span>
<span data-ttu-id="1cbca-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1cbca-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1cbca-124">-WebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-124">-WebApp</span></span>
<span data-ttu-id="1cbca-125">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-125">WebApp Object</span></span>

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

### <span data-ttu-id="1cbca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cbca-126">-Confirm</span></span>
<span data-ttu-id="1cbca-127">Запрос на подтверждение перед запуском cmdlet. Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbca-127">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cbca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cbca-128">-WhatIf</span></span>
<span data-ttu-id="1cbca-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cbca-130">Этот cmdlet не будет выполниться. Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cbca-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cbca-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1cbca-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cbca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cbca-132">CommonParameters</span></span>
<span data-ttu-id="1cbca-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cbca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cbca-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cbca-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cbca-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1cbca-135">INPUTS</span></span>

### <span data-ttu-id="1cbca-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1cbca-136">System.String</span></span>

### <span data-ttu-id="1cbca-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="1cbca-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="1cbca-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1cbca-138">OUTPUTS</span></span>

### <span data-ttu-id="1cbca-139">System.Void</span><span class="sxs-lookup"><span data-stu-id="1cbca-139">System.Void</span></span>

## <span data-ttu-id="1cbca-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1cbca-140">NOTES</span></span>

## <span data-ttu-id="1cbca-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cbca-141">RELATED LINKS</span></span>

[<span data-ttu-id="1cbca-142">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-142">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="1cbca-143">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-143">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="1cbca-144">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-144">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="1cbca-145">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-145">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="1cbca-146">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="1cbca-146">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


