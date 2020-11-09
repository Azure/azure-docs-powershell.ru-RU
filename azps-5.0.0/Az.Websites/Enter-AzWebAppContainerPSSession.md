---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/enter-azwebappcontainerpssession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Enter-AzWebAppContainerPSSession.md
ms.openlocfilehash: ddf728a1340d763c1feb2ba313a2dc73494b5d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247956"
---
# <span data-ttu-id="03c5c-101">Enter-AzWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="03c5c-101">Enter-AzWebAppContainerPSSession</span></span>

## <span data-ttu-id="03c5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03c5c-102">SYNOPSIS</span></span>
<span data-ttu-id="03c5c-103">Открытие удаленного сеанса PowerShell в контейнере Windows, указанном на данном сайте или в области, и данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03c5c-103">Opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="03c5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03c5c-104">SYNTAX</span></span>

### <span data-ttu-id="03c5c-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03c5c-105">S1 (Default)</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03c5c-106">S2</span><span class="sxs-lookup"><span data-stu-id="03c5c-106">S2</span></span>
```
Enter-AzWebAppContainerPSSession [-PassThru] [-Force] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03c5c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03c5c-107">DESCRIPTION</span></span>
<span data-ttu-id="03c5c-108">открытие удаленного сеанса PowerShell в контейнере Windows, указанном на данном сайте или в области, и данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03c5c-108">opens a remote PowerShell session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="03c5c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03c5c-109">EXAMPLES</span></span>

### <span data-ttu-id="03c5c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03c5c-110">Example 1</span></span>
```
PS C:\> Enter-AzWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="03c5c-111">Эта команда открывает удаленный сеанс PowerShell в приложении контейнера Windows ContosoASP</span><span class="sxs-lookup"><span data-stu-id="03c5c-111">This command opens a remote PowerShell session into the windows container app ContosoASP</span></span>

## <span data-ttu-id="03c5c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03c5c-112">PARAMETERS</span></span>

### <span data-ttu-id="03c5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c5c-113">-DefaultProfile</span></span>
<span data-ttu-id="03c5c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03c5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03c5c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="03c5c-115">-Force</span></span>
<span data-ttu-id="03c5c-116">Создайте сеанс PowerShell без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="03c5c-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="03c5c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03c5c-117">-Name</span></span>
<span data-ttu-id="03c5c-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="03c5c-118">The name of the web app.</span></span>

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

### <span data-ttu-id="03c5c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03c5c-119">-PassThru</span></span>
<span data-ttu-id="03c5c-120">Возвращение значения, показывающего успешное выполнение или сбой</span><span class="sxs-lookup"><span data-stu-id="03c5c-120">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="03c5c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c5c-121">-ResourceGroupName</span></span>
<span data-ttu-id="03c5c-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="03c5c-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="03c5c-123">-SlotName</span><span class="sxs-lookup"><span data-stu-id="03c5c-123">-SlotName</span></span>
<span data-ttu-id="03c5c-124">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="03c5c-124">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03c5c-125">-WebApp</span><span class="sxs-lookup"><span data-stu-id="03c5c-125">-WebApp</span></span>
<span data-ttu-id="03c5c-126">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="03c5c-126">The web app object</span></span>

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

### <span data-ttu-id="03c5c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03c5c-127">-Confirm</span></span>
<span data-ttu-id="03c5c-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03c5c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03c5c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03c5c-129">-WhatIf</span></span>
<span data-ttu-id="03c5c-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03c5c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03c5c-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03c5c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03c5c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c5c-132">CommonParameters</span></span>
<span data-ttu-id="03c5c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03c5c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c5c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03c5c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c5c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03c5c-135">INPUTS</span></span>

### <span data-ttu-id="03c5c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="03c5c-136">System.String</span></span>

### <span data-ttu-id="03c5c-137">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="03c5c-137">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="03c5c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03c5c-138">OUTPUTS</span></span>

### <span data-ttu-id="03c5c-139">System. void</span><span class="sxs-lookup"><span data-stu-id="03c5c-139">System.Void</span></span>

## <span data-ttu-id="03c5c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="03c5c-140">NOTES</span></span>

## <span data-ttu-id="03c5c-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03c5c-141">RELATED LINKS</span></span>