---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 99865242-6623-425E-92F2-0B229FC4EDAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsLinuxCustomLogCollection.md
ms.openlocfilehash: 0b907f07280eae32ecb208fd13195767145c9541
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567555"
---
# <span data-ttu-id="65c63-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="65c63-101">Enable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>

## <span data-ttu-id="65c63-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="65c63-102">SYNOPSIS</span></span>
<span data-ttu-id="65c63-103">Запускает сбор настраиваемых журналов на компьютерах с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="65c63-103">Starts collection of custom logs from Linux computers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65c63-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="65c63-104">SYNTAX</span></span>

### <span data-ttu-id="65c63-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="65c63-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-ResourceGroupName] <String>
 [-WorkspaceName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65c63-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="65c63-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsLinuxCustomLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65c63-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c63-107">DESCRIPTION</span></span>
<span data-ttu-id="65c63-108">Командлет **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** запускает сбор настраиваемых журналов из подключенных компьютеров Linux в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="65c63-108">The **Enable-AzureRmOperationalInsightsLinuxCustomLogCollection** cmdlet starts collection of custom logs from connected Linux computers in a workspace.</span></span>

## <span data-ttu-id="65c63-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="65c63-109">EXAMPLES</span></span>

## <span data-ttu-id="65c63-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="65c63-110">PARAMETERS</span></span>

### <span data-ttu-id="65c63-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65c63-111">-ResourceGroupName</span></span>
<span data-ttu-id="65c63-112">Указывает имя группы ресурсов, которая содержит компьютеры Linux.</span><span class="sxs-lookup"><span data-stu-id="65c63-112">Specifies the name of a resource group that contains Linux computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c63-113">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="65c63-113">-Workspace</span></span>
<span data-ttu-id="65c63-114">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="65c63-114">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="65c63-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="65c63-115">-WorkspaceName</span></span>
<span data-ttu-id="65c63-116">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="65c63-116">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65c63-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="65c63-117">-Confirm</span></span>
<span data-ttu-id="65c63-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="65c63-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65c63-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65c63-119">-WhatIf</span></span>
<span data-ttu-id="65c63-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="65c63-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65c63-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="65c63-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65c63-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65c63-122">-DefaultProfile</span></span>
<span data-ttu-id="65c63-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65c63-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65c63-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65c63-124">CommonParameters</span></span>
<span data-ttu-id="65c63-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="65c63-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65c63-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65c63-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65c63-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="65c63-127">INPUTS</span></span>

### <span data-ttu-id="65c63-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="65c63-128">PSWorkspace</span></span>
<span data-ttu-id="65c63-129">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="65c63-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="65c63-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="65c63-130">OUTPUTS</span></span>

### <span data-ttu-id="65c63-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="65c63-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="65c63-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="65c63-132">NOTES</span></span>
* <span data-ttu-id="65c63-133">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, эксплуатация, аналитика</span><span class="sxs-lookup"><span data-stu-id="65c63-133">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="65c63-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65c63-134">RELATED LINKS</span></span>

[<span data-ttu-id="65c63-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span><span class="sxs-lookup"><span data-stu-id="65c63-135">Disable-AzureRmOperationalInsightsLinuxCustomLogCollection</span></span>](./Disable-AzureRmOperationalInsightsLinuxCustomLogCollection.md)


