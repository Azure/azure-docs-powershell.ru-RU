---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Remove-AzureRmWebApp.md
ms.openlocfilehash: b903e22a627ca2cb992b179e8f6956d556558b6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569128"
---
# <span data-ttu-id="ef22f-101">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-101">Remove-AzureRmWebApp</span></span>

## <span data-ttu-id="ef22f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef22f-102">SYNOPSIS</span></span>
<span data-ttu-id="ef22f-103">Удаление веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="ef22f-103">Removes an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef22f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef22f-104">SYNTAX</span></span>

### <span data-ttu-id="ef22f-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="ef22f-105">S1</span></span>
```
Remove-AzureRmWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ef22f-106">S2</span><span class="sxs-lookup"><span data-stu-id="ef22f-106">S2</span></span>
```
Remove-AzureRmWebApp [-Force] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef22f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef22f-107">DESCRIPTION</span></span>
<span data-ttu-id="ef22f-108">Командлет **Remove-AzureRmWebApp** удаляет веб-приложение Azure, которое предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="ef22f-108">The **Remove-AzureRmWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="ef22f-109">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="ef22f-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="ef22f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef22f-110">EXAMPLES</span></span>

### <span data-ttu-id="ef22f-111">Пример 1: удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="ef22f-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="ef22f-112">Эта команда удаляет веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="ef22f-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="ef22f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef22f-113">PARAMETERS</span></span>

### <span data-ttu-id="ef22f-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ef22f-114">-Force</span></span>
<span data-ttu-id="ef22f-115">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="ef22f-115">Forcefully Remove Option</span></span>

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

### <span data-ttu-id="ef22f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef22f-116">-Name</span></span>
<span data-ttu-id="ef22f-117">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-117">WebApp Name</span></span>

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

### <span data-ttu-id="ef22f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef22f-118">-ResourceGroupName</span></span>
<span data-ttu-id="ef22f-119">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ef22f-119">Resource Group Name</span></span>

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

### <span data-ttu-id="ef22f-120">-WebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-120">-WebApp</span></span>
<span data-ttu-id="ef22f-121">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-121">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef22f-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef22f-122">-Confirm</span></span>
<span data-ttu-id="ef22f-123">Запрашивает подтверждение перед запуском командлета. Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef22f-123">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef22f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef22f-124">-WhatIf</span></span>
<span data-ttu-id="ef22f-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef22f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef22f-126">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef22f-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef22f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef22f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef22f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef22f-128">-DefaultProfile</span></span>
<span data-ttu-id="ef22f-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef22f-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef22f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef22f-130">CommonParameters</span></span>
<span data-ttu-id="ef22f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef22f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef22f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef22f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef22f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef22f-133">INPUTS</span></span>

### <span data-ttu-id="ef22f-134">Семейств</span><span class="sxs-lookup"><span data-stu-id="ef22f-134">Site</span></span>
<span data-ttu-id="ef22f-135">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ef22f-135">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="ef22f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef22f-136">OUTPUTS</span></span>

## <span data-ttu-id="ef22f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef22f-137">NOTES</span></span>

## <span data-ttu-id="ef22f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef22f-138">RELATED LINKS</span></span>

[<span data-ttu-id="ef22f-139">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-139">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="ef22f-140">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-140">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="ef22f-141">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-141">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="ef22f-142">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-142">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="ef22f-143">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="ef22f-143">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


