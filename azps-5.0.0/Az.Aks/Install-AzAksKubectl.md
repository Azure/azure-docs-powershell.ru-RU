---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318743"
---
# <span data-ttu-id="db295-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="db295-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="db295-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db295-102">SYNOPSIS</span></span>
<span data-ttu-id="db295-103">Скачайте и установите kubectl с помощью средства командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="db295-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="db295-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db295-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db295-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db295-105">DESCRIPTION</span></span>
<span data-ttu-id="db295-106">Скачайте и установите kubectl с помощью средства командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="db295-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="db295-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db295-107">EXAMPLES</span></span>

### <span data-ttu-id="db295-108">Скачайте и установите последнюю версию kubectl</span><span class="sxs-lookup"><span data-stu-id="db295-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="db295-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db295-109">PARAMETERS</span></span>

### <span data-ttu-id="db295-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db295-110">-AsJob</span></span>
<span data-ttu-id="db295-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="db295-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="db295-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db295-112">-DefaultProfile</span></span>
<span data-ttu-id="db295-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db295-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db295-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="db295-114">-Destination</span></span>
<span data-ttu-id="db295-115">Путь для установки kubectl.</span><span class="sxs-lookup"><span data-stu-id="db295-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="db295-116">Установка по умолчанию в ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="db295-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="db295-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="db295-117">-DownloadFromMirror</span></span>
<span data-ttu-id="db295-118">Загрузка из зеркального сайта: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="db295-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="db295-119">-Force</span><span class="sxs-lookup"><span data-stu-id="db295-119">-Force</span></span>
<span data-ttu-id="db295-120">Перезаписать существующий kubectl без запроса</span><span class="sxs-lookup"><span data-stu-id="db295-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="db295-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db295-121">-PassThru</span></span>
<span data-ttu-id="db295-122">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="db295-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="db295-123">-Version</span><span class="sxs-lookup"><span data-stu-id="db295-123">-Version</span></span>
<span data-ttu-id="db295-124">Устанавливаемая версия kubectl, например "v 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="db295-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="db295-125">Значение по умолчанию: Последнее</span><span class="sxs-lookup"><span data-stu-id="db295-125">Default value: Latest</span></span>

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

### <span data-ttu-id="db295-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db295-126">-Confirm</span></span>
<span data-ttu-id="db295-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db295-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db295-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db295-128">-WhatIf</span></span>
<span data-ttu-id="db295-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db295-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db295-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db295-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db295-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db295-131">CommonParameters</span></span>
<span data-ttu-id="db295-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db295-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db295-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db295-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db295-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db295-134">INPUTS</span></span>

### <span data-ttu-id="db295-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="db295-135">None</span></span>

## <span data-ttu-id="db295-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db295-136">OUTPUTS</span></span>

### <span data-ttu-id="db295-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="db295-137">System.Boolean</span></span>

## <span data-ttu-id="db295-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="db295-138">NOTES</span></span>

## <span data-ttu-id="db295-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db295-139">RELATED LINKS</span></span>
