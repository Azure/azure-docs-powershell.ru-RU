---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 26B1921E-6052-471B-B5B6-F2853536A425
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/enable-azurermoperationalinsightsiislogcollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Enable-AzureRmOperationalInsightsIISLogCollection.md
ms.openlocfilehash: 417bc080d707c3da02dd8a0083fb707f79d0a999
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564700"
---
# <span data-ttu-id="da82d-101">Enable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="da82d-101">Enable-AzureRmOperationalInsightsIISLogCollection</span></span>

## <span data-ttu-id="da82d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da82d-102">SYNOPSIS</span></span>
<span data-ttu-id="da82d-103">Запускает сбор журналов IIS на компьютерах в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="da82d-103">Starts collection of IIS logs from computers in a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da82d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da82d-104">SYNTAX</span></span>

### <span data-ttu-id="da82d-105">ByWorkspaceName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="da82d-105">ByWorkspaceName (Default)</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da82d-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="da82d-106">ByWorkspaceObject</span></span>
```
Enable-AzureRmOperationalInsightsIISLogCollection [-Workspace] <PSWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da82d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da82d-107">DESCRIPTION</span></span>
<span data-ttu-id="da82d-108">Командлет **Enable-AzureRmOperationalInsightsIISLogCollection** запускает сбор журналов служб IIS с подключенных компьютеров в рабочей области.</span><span class="sxs-lookup"><span data-stu-id="da82d-108">The **Enable-AzureRmOperationalInsightsIISLogCollection** cmdlet starts collection of Internet Information Services (IIS) logs from connected computers in a workspace.</span></span>

## <span data-ttu-id="da82d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da82d-109">EXAMPLES</span></span>

## <span data-ttu-id="da82d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da82d-110">PARAMETERS</span></span>

### <span data-ttu-id="da82d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da82d-111">-DefaultProfile</span></span>
<span data-ttu-id="da82d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="da82d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da82d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da82d-113">-ResourceGroupName</span></span>
<span data-ttu-id="da82d-114">Указывает имя группы ресурсов, содержащей компьютеры.</span><span class="sxs-lookup"><span data-stu-id="da82d-114">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da82d-115">-Рабочая область</span><span class="sxs-lookup"><span data-stu-id="da82d-115">-Workspace</span></span>
<span data-ttu-id="da82d-116">Указывает рабочую область, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da82d-116">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da82d-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da82d-117">-WorkspaceName</span></span>
<span data-ttu-id="da82d-118">Указывает имя рабочей области, в которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da82d-118">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da82d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="da82d-119">-Confirm</span></span>
<span data-ttu-id="da82d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="da82d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da82d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da82d-121">-WhatIf</span></span>
<span data-ttu-id="da82d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="da82d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da82d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="da82d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da82d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da82d-124">CommonParameters</span></span>
<span data-ttu-id="da82d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da82d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da82d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da82d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da82d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da82d-127">INPUTS</span></span>

### <span data-ttu-id="da82d-128">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="da82d-128">PSWorkspace</span></span>
<span data-ttu-id="da82d-129">Параметр "Рабочая область" принимает значение типа "PSWorkspace" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="da82d-129">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="da82d-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da82d-130">OUTPUTS</span></span>

### <span data-ttu-id="da82d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span><span class="sxs-lookup"><span data-stu-id="da82d-131">Microsoft.Azure.Commands.OperationalInsights.Models.PSDataSource</span></span>

## <span data-ttu-id="da82d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="da82d-132">NOTES</span></span>

## <span data-ttu-id="da82d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da82d-133">RELATED LINKS</span></span>

[<span data-ttu-id="da82d-134">Disable-AzureRmOperationalInsightsIISLogCollection</span><span class="sxs-lookup"><span data-stu-id="da82d-134">Disable-AzureRmOperationalInsightsIISLogCollection</span></span>](./Disable-AzureRmOperationalInsightsIISLogCollection.md)


