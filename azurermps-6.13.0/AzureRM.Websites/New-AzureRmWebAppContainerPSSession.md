---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppContainerPSSession.md
ms.openlocfilehash: 3c5efcd51a8b546acb5fa9b8ed3623c40ddfb1e0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558119"
---
# <span data-ttu-id="9b001-101">New-AzureRmWebAppContainerPSSession</span><span class="sxs-lookup"><span data-stu-id="9b001-101">New-AzureRmWebAppContainerPSSession</span></span>

## <span data-ttu-id="9b001-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b001-102">SYNOPSIS</span></span>
<span data-ttu-id="9b001-103">New-AzureRmWebAppContainerPSSession создаст новый сеанс удаленной оболочки PowerShell в контейнере Windows, указанном на данном сайте или в области, и заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b001-103">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b001-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b001-104">SYNTAX</span></span>

### <span data-ttu-id="9b001-105">S1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b001-105">S1 (Default)</span></span>
```
New-AzureRmWebAppContainerPSSession [[-SlotName] <String>] [-Force] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b001-106">S2</span><span class="sxs-lookup"><span data-stu-id="9b001-106">S2</span></span>
```
New-AzureRmWebAppContainerPSSession [-Force] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b001-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b001-107">DESCRIPTION</span></span>
<span data-ttu-id="9b001-108">New-AzureRmWebAppContainerPSSession создаст новый сеанс удаленной оболочки PowerShell в контейнере Windows, указанном на данном сайте или в области, и заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b001-108">New-AzureRmWebAppContainerPSSession will create new remote PowerShell Session into the windows container specified in a given site or slot and given resource group</span></span>

## <span data-ttu-id="9b001-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b001-109">EXAMPLES</span></span>

### <span data-ttu-id="9b001-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9b001-110">Example 1</span></span>
```
PS C:\> $s = New-AzureRmWebAppContainerPSSession -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
PS C:\> Invoke-Command -Session $s -ScriptBlock{Get-Process}
```

<span data-ttu-id="9b001-111">Это приведет к созданию нового сеанса PowerShell в приложении контейнера Windows ContosoASP и отображения процессов, которые выполняются в контейнере ContosoASP</span><span class="sxs-lookup"><span data-stu-id="9b001-111">This will create a new remote PowerShell Session into the windows container app ContosoASP and show the processes that are running on the container ContosoASP</span></span>

## <span data-ttu-id="9b001-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b001-112">PARAMETERS</span></span>

### <span data-ttu-id="9b001-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b001-113">-DefaultProfile</span></span>
<span data-ttu-id="9b001-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b001-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b001-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9b001-115">-Force</span></span>
<span data-ttu-id="9b001-116">Создайте сеанс PowerShell без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="9b001-116">Create the PowerShell session without prompting for confirmation.</span></span>

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

### <span data-ttu-id="9b001-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9b001-117">-Name</span></span>
<span data-ttu-id="9b001-118">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9b001-118">The name of the web app.</span></span>

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

### <span data-ttu-id="9b001-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b001-119">-ResourceGroupName</span></span>
<span data-ttu-id="9b001-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b001-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="9b001-121">-SlotName</span><span class="sxs-lookup"><span data-stu-id="9b001-121">-SlotName</span></span>
<span data-ttu-id="9b001-122">Имя области веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9b001-122">The name of the web app slot.</span></span>

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

### <span data-ttu-id="9b001-123">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9b001-123">-WebApp</span></span>
<span data-ttu-id="9b001-124">Объект веб-приложения</span><span class="sxs-lookup"><span data-stu-id="9b001-124">The web app object</span></span>

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

### <span data-ttu-id="9b001-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b001-125">-Confirm</span></span>
<span data-ttu-id="9b001-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9b001-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b001-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b001-127">-WhatIf</span></span>
<span data-ttu-id="9b001-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9b001-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9b001-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9b001-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b001-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b001-130">CommonParameters</span></span>
<span data-ttu-id="9b001-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b001-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b001-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b001-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b001-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b001-133">INPUTS</span></span>

### <span data-ttu-id="9b001-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9b001-134">System.String</span></span>
### <span data-ttu-id="9b001-135">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="9b001-135">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="9b001-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b001-136">OUTPUTS</span></span>

### <span data-ttu-id="9b001-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9b001-137">System.String</span></span>
## <span data-ttu-id="9b001-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b001-138">NOTES</span></span>

## <span data-ttu-id="9b001-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b001-139">RELATED LINKS</span></span>
