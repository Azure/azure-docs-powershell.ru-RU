---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/install-azakskubectl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Install-AzAksKubectl.md
ms.openlocfilehash: 746efc579e1977e54a1898bbe183d951c3d9c21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235167"
---
# <span data-ttu-id="c45d1-101">Install-AzAksKubectl</span><span class="sxs-lookup"><span data-stu-id="c45d1-101">Install-AzAksKubectl</span></span>

## <span data-ttu-id="c45d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c45d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c45d1-103">Скачайте и установите kubectl с помощью средства командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c45d1-103">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c45d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c45d1-104">SYNTAX</span></span>

```
Install-AzAksKubectl [-Destination <String>] [-Version <String>] [-DownloadFromMirror] [-PassThru] [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c45d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c45d1-105">DESCRIPTION</span></span>
<span data-ttu-id="c45d1-106">Скачайте и установите kubectl с помощью средства командной строки Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c45d1-106">Download and install kubectl, the Kubernetes command-line tool.</span></span>

## <span data-ttu-id="c45d1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c45d1-107">EXAMPLES</span></span>

### <span data-ttu-id="c45d1-108">Скачайте и установите последнюю версию kubectl</span><span class="sxs-lookup"><span data-stu-id="c45d1-108">Download and install latest version of kubectl</span></span>
```powershell
PS C:\> Install-AzAksKubectl -Version latest
```

## <span data-ttu-id="c45d1-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c45d1-109">PARAMETERS</span></span>

### <span data-ttu-id="c45d1-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c45d1-110">-AsJob</span></span>
<span data-ttu-id="c45d1-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c45d1-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c45d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c45d1-112">-DefaultProfile</span></span>
<span data-ttu-id="c45d1-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c45d1-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c45d1-114">-Destination</span><span class="sxs-lookup"><span data-stu-id="c45d1-114">-Destination</span></span>
<span data-ttu-id="c45d1-115">Путь для установки kubectl.</span><span class="sxs-lookup"><span data-stu-id="c45d1-115">Path at which to install kubectl.</span></span>
<span data-ttu-id="c45d1-116">Установка по умолчанию в ~/.Azure-kubectl/</span><span class="sxs-lookup"><span data-stu-id="c45d1-116">Default to install into ~/.azure-kubectl/</span></span>

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

### <span data-ttu-id="c45d1-117">-DownloadFromMirror</span><span class="sxs-lookup"><span data-stu-id="c45d1-117">-DownloadFromMirror</span></span>
<span data-ttu-id="c45d1-118">Загрузка из зеркального сайта: https://mirror.azure.cn/kubernetes/kubectl/</span><span class="sxs-lookup"><span data-stu-id="c45d1-118">Download from mirror site : https://mirror.azure.cn/kubernetes/kubectl/</span></span>

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

### <span data-ttu-id="c45d1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c45d1-119">-Force</span></span>
<span data-ttu-id="c45d1-120">Перезаписать существующий kubectl без запроса</span><span class="sxs-lookup"><span data-stu-id="c45d1-120">Overwrite existing kubectl without prompt</span></span>

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

### <span data-ttu-id="c45d1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c45d1-121">-PassThru</span></span>
<span data-ttu-id="c45d1-122">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c45d1-122">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="c45d1-123">-Version</span><span class="sxs-lookup"><span data-stu-id="c45d1-123">-Version</span></span>
<span data-ttu-id="c45d1-124">Устанавливаемая версия kubectl, например "v 1.17.2".</span><span class="sxs-lookup"><span data-stu-id="c45d1-124">Version of kubectl to install, e.g. 'v1.17.2'.</span></span>
<span data-ttu-id="c45d1-125">Значение по умолчанию: Последнее</span><span class="sxs-lookup"><span data-stu-id="c45d1-125">Default value: Latest</span></span>

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

### <span data-ttu-id="c45d1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c45d1-126">-Confirm</span></span>
<span data-ttu-id="c45d1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c45d1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c45d1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c45d1-128">-WhatIf</span></span>
<span data-ttu-id="c45d1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c45d1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c45d1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c45d1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c45d1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c45d1-131">CommonParameters</span></span>
<span data-ttu-id="c45d1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c45d1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c45d1-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c45d1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c45d1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c45d1-134">INPUTS</span></span>

### <span data-ttu-id="c45d1-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="c45d1-135">None</span></span>

## <span data-ttu-id="c45d1-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c45d1-136">OUTPUTS</span></span>

### <span data-ttu-id="c45d1-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c45d1-137">System.Boolean</span></span>

## <span data-ttu-id="c45d1-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c45d1-138">NOTES</span></span>

## <span data-ttu-id="c45d1-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c45d1-139">RELATED LINKS</span></span>
