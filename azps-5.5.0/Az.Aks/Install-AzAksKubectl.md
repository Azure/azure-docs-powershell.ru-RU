---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233921"
---
# <span data-ttu-id="cb976-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="cb976-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="cb976-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb976-102">SYNOPSIS</span></span>
<span data-ttu-id="cb976-103">Скачайте и установите инструмент командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cb976-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="cb976-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb976-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb976-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb976-105">DESCRIPTION</span></span>
<span data-ttu-id="cb976-106">Скачайте и установите инструмент командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cb976-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="cb976-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb976-107">EXAMPLES</span></span>

### <span data-ttu-id="cb976-108">Скачивание и установка последней версии kubectl</span><span class="sxs-lookup"><span data-stu-id="cb976-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="cb976-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb976-109">PARAMETERS</span></span>

### <span data-ttu-id="cb976-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb976-110">-AsJob</span></span>
<span data-ttu-id="cb976-111">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cb976-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cb976-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb976-112">-DefaultProfile</span></span>
<span data-ttu-id="cb976-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb976-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb976-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="cb976-114">-Destination</span></span>
<span data-ttu-id="cb976-115">Путь, по которому нужно установить кюбокль.</span><span class="sxs-lookup"><span data-stu-id="cb976-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="cb976-116">Значение по умолчанию для установки в ~/.azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="cb976-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="cb976-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="cb976-117">-DownloadFromMirror</span></span>
<span data-ttu-id="cb976-118">Скачать с зеркального сайта: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="cb976-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="cb976-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cb976-119">-Force</span></span>
<span data-ttu-id="cb976-120">Переописывать существующие кюбки без запроса</span><span class="sxs-lookup"><span data-stu-id="cb976-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="cb976-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cb976-121">-PassThru</span></span>
<span data-ttu-id="cb976-122">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="cb976-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="cb976-123">-Version</span><span class="sxs-lookup"><span data-stu-id="cb976-123">-Version</span></span>
<span data-ttu-id="cb976-124">Версия kubectl для установки, например "версия 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="cb976-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="cb976-125">Значение по умолчанию: Последняя</span><span class="sxs-lookup"><span data-stu-id="cb976-125">Default value: Latest</span></span>

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

### <span data-ttu-id="cb976-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb976-126">-Confirm</span></span>
<span data-ttu-id="cb976-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cb976-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb976-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb976-128">-WhatIf</span></span>
<span data-ttu-id="cb976-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb976-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb976-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb976-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb976-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb976-131">CommonParameters</span></span>
<span data-ttu-id="cb976-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb976-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb976-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb976-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb976-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb976-134">INPUTS</span></span>

### <span data-ttu-id="cb976-135">Нет</span><span class="sxs-lookup"><span data-stu-id="cb976-135">None</span></span>

## <span data-ttu-id="cb976-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb976-136">OUTPUTS</span></span>

### <span data-ttu-id="cb976-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cb976-137">System.Boolean</span></span>

## <span data-ttu-id="cb976-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb976-138">NOTES</span></span>

## <span data-ttu-id="cb976-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb976-139">RELATED LINKS</span></span>
