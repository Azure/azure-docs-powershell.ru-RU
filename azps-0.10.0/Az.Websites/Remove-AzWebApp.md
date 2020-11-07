---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 9057185C-6F22-4C4A-8480-BE542B5D6BAF
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/remove-Azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Remove-AzWebApp.md
ms.openlocfilehash: 40b14128ec2a1dc48cf098a2c0427728c34c7e22
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910590"
---
# <span data-ttu-id="bb6dc-101">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-101">Remove-AzWebApp</span></span>

## <span data-ttu-id="bb6dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="bb6dc-103">Удаление веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-103">Removes an Azure Web App.</span></span>

## <span data-ttu-id="bb6dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb6dc-104">SYNTAX</span></span>

### <span data-ttu-id="bb6dc-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="bb6dc-105">S1</span></span>
```
Remove-AzWebApp [-Force] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb6dc-106">S2</span><span class="sxs-lookup"><span data-stu-id="bb6dc-106">S2</span></span>
```
Remove-AzWebApp [-Force] [-WebApp] <Site> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb6dc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6dc-107">DESCRIPTION</span></span>
<span data-ttu-id="bb6dc-108">Командлет **Remove-AzWebApp** удаляет веб-приложение Azure, которое предоставил группу ресурсов и имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-108">The **Remove-AzWebApp** cmdlet removes an Azure Web App provided the resource group and Web App name.</span></span>
<span data-ttu-id="bb6dc-109">Этот командлет по умолчанию также удаляет все слоты и метрики.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-109">This cmdlet, by default, also removes all slots and metrics.</span></span>

## <span data-ttu-id="bb6dc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb6dc-110">EXAMPLES</span></span>

### <span data-ttu-id="bb6dc-111">Пример 1: удаление веб-приложения</span><span class="sxs-lookup"><span data-stu-id="bb6dc-111">Example 1: Remove a Web App</span></span>
```
PS C:\>Remove-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="bb6dc-112">Эта команда удаляет веб-приложение Azure с именем ContosoSite, которое принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-112">This command removes the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="bb6dc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb6dc-113">PARAMETERS</span></span>

### <span data-ttu-id="bb6dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb6dc-114">-DefaultProfile</span></span>
<span data-ttu-id="bb6dc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bb6dc-116">-Force</span></span>
<span data-ttu-id="bb6dc-117">Параметр принудительного удаления</span><span class="sxs-lookup"><span data-stu-id="bb6dc-117">Forcefully Remove Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bb6dc-118">-Name</span></span>
<span data-ttu-id="bb6dc-119">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-119">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb6dc-120">-ResourceGroupName</span></span>
<span data-ttu-id="bb6dc-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="bb6dc-121">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-122">-WebApp</span></span>
<span data-ttu-id="bb6dc-123">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-123">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bb6dc-124">-Confirm</span></span>
<span data-ttu-id="bb6dc-125">Запрашивает подтверждение перед запуском командлета. Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-125">Prompts you for confirmation before running the cmdlet.Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb6dc-126">-WhatIf</span></span>
<span data-ttu-id="bb6dc-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6dc-128">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-128">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb6dc-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bb6dc-130">-AsJob</span></span>
<span data-ttu-id="bb6dc-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bb6dc-131">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb6dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb6dc-132">CommonParameters</span></span>
<span data-ttu-id="bb6dc-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb6dc-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb6dc-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb6dc-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb6dc-135">INPUTS</span></span>

### <span data-ttu-id="bb6dc-136">Семейств</span><span class="sxs-lookup"><span data-stu-id="bb6dc-136">Site</span></span>
<span data-ttu-id="bb6dc-137">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bb6dc-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bb6dc-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb6dc-138">OUTPUTS</span></span>

## <span data-ttu-id="bb6dc-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb6dc-139">NOTES</span></span>

## <span data-ttu-id="bb6dc-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb6dc-140">RELATED LINKS</span></span>

[<span data-ttu-id="bb6dc-141">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-141">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="bb6dc-142">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-142">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="bb6dc-143">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-143">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="bb6dc-144">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-144">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="bb6dc-145">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="bb6dc-145">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


