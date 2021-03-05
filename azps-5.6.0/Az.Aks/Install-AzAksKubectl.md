---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 6a3dc975c34d4938235ce95743f73f833a948b49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966851"
---
# <span data-ttu-id="be388-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="be388-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="be388-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be388-102">SYNOPSIS</span></span>
<span data-ttu-id="be388-103">Скачайте и установите кубект, инструмент командной строки "Кубберсеть".</span><span class="sxs-lookup"><span data-stu-id="be388-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="be388-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="be388-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be388-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be388-105">DESCRIPTION</span></span>
<span data-ttu-id="be388-106">Скачайте и установите кубект, инструмент командной строки "Кубберсеть".</span><span class="sxs-lookup"><span data-stu-id="be388-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="be388-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="be388-107">EXAMPLES</span></span>

### <span data-ttu-id="be388-108">Скачивание и установка последней версии kubectl</span><span class="sxs-lookup"><span data-stu-id="be388-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="be388-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be388-109">PARAMETERS</span></span>

### <span data-ttu-id="be388-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be388-110">-AsJob</span></span>
<span data-ttu-id="be388-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="be388-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="be388-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be388-112">-DefaultProfile</span></span>
<span data-ttu-id="be388-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be388-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be388-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="be388-114">-Destination</span></span>
<span data-ttu-id="be388-115">Путь, на котором нужно установить кюбокль.</span><span class="sxs-lookup"><span data-stu-id="be388-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="be388-116">Значение по умолчанию для установки в ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="be388-116">Default to install into ~/.azure-kubectl/</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be388-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="be388-117">-DownloadFromMirror</span></span>
<span data-ttu-id="be388-118">Скачать с зеркального сайта: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="be388-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="be388-119">-Force</span><span class="sxs-lookup"><span data-stu-id="be388-119">-Force</span></span>
<span data-ttu-id="be388-120">Переописывать существующие кюбки без запроса</span><span class="sxs-lookup"><span data-stu-id="be388-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="be388-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be388-121">-PassThru</span></span>
<span data-ttu-id="be388-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="be388-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="be388-123">-Version</span><span class="sxs-lookup"><span data-stu-id="be388-123">-Version</span></span>
<span data-ttu-id="be388-124">Версия kubectl для установки, например "версия 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="be388-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="be388-125">Значение по умолчанию: последняя</span><span class="sxs-lookup"><span data-stu-id="be388-125">Default value: Latest</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be388-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be388-126">-Confirm</span></span>
<span data-ttu-id="be388-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be388-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be388-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be388-128">-WhatIf</span></span>
<span data-ttu-id="be388-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be388-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be388-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="be388-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be388-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be388-131">CommonParameters</span></span>
<span data-ttu-id="be388-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be388-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be388-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be388-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be388-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="be388-134">INPUTS</span></span>

### <span data-ttu-id="be388-135">Нет</span><span class="sxs-lookup"><span data-stu-id="be388-135">None</span></span>

## <span data-ttu-id="be388-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="be388-136">OUTPUTS</span></span>

### <span data-ttu-id="be388-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="be388-137">System.Boolean</span></span>

## <span data-ttu-id="be388-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="be388-138">NOTES</span></span>

## <span data-ttu-id="be388-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be388-139">RELATED LINKS</span></span>
