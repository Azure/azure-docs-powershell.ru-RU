---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceExtensionObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceExtensionObject.md
ms.openlocfilehash: 761d34b4ed2d061b773c136a7d4e2db9f05a9103
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229204"
---
# <span data-ttu-id="da745-101">New-AzCloudServiceExtensionObject</span><span class="sxs-lookup"><span data-stu-id="da745-101">New-AzCloudServiceExtensionObject</span></span>

## <span data-ttu-id="da745-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da745-102">SYNOPSIS</span></span>
<span data-ttu-id="da745-103">Создание объекта в памяти для расширения</span><span class="sxs-lookup"><span data-stu-id="da745-103">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="da745-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da745-104">SYNTAX</span></span>

```
New-AzCloudServiceExtensionObject [-AutoUpgradeMinorVersion <Boolean>] [-Name <String>]
 [-ProtectedSetting <String>] [-Publisher <String>] [-RolesAppliedTo <String[]>] [-Setting <String>]
 [-Type <String>] [-TypeHandlerVersion <String>] [<CommonParameters>]
```

## <span data-ttu-id="da745-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da745-105">DESCRIPTION</span></span>
<span data-ttu-id="da745-106">Создание объекта в памяти для расширения</span><span class="sxs-lookup"><span data-stu-id="da745-106">Create a in-memory object for Extension</span></span>

## <span data-ttu-id="da745-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da745-107">EXAMPLES</span></span>

### <span data-ttu-id="da745-108">Пример 1. Создание объекта расширения Для вех</span><span class="sxs-lookup"><span data-stu-id="da745-108">Example 1: Create Geneva extension object</span></span>
```powershell
PS C:\> $extension = New-AzCloudServiceExtensionObject -Name "GenevaExtension" -Publisher "Microsoft.Azure.Geneva" -Type "GenevaMonitoringPaaS" -TypeHandlerVersion "2.14.0.2"
```

<span data-ttu-id="da745-109">Эта команда создает объект расширения Висяча, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="da745-109">This command creates Geneva extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="da745-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="da745-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="da745-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da745-111">PARAMETERS</span></span>

### <span data-ttu-id="da745-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="da745-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="da745-113">Явным образом укажите, можно ли автоматически обновлять typeHandlerVersion до более высоких версий, когда они становятся доступны.</span><span class="sxs-lookup"><span data-stu-id="da745-113">Explicitly specify whether CRP can automatically upgrade typeHandlerVersion to higher minor versions when they become available.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da745-114">-Name</span><span class="sxs-lookup"><span data-stu-id="da745-114">-Name</span></span>
<span data-ttu-id="da745-115">Имя.</span><span class="sxs-lookup"><span data-stu-id="da745-115">Name.</span></span>

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

### <span data-ttu-id="da745-116">-ProtectedSetting</span><span class="sxs-lookup"><span data-stu-id="da745-116">-ProtectedSetting</span></span>
<span data-ttu-id="da745-117">Защищенные параметры расширения, которые шифруются перед его отправлением в VM-</span><span class="sxs-lookup"><span data-stu-id="da745-117">Protected settings for the extension which are encrypted before sent to the VM.</span></span>

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

### <span data-ttu-id="da745-118">-Publisher</span><span class="sxs-lookup"><span data-stu-id="da745-118">-Publisher</span></span>
<span data-ttu-id="da745-119">Publisher.</span><span class="sxs-lookup"><span data-stu-id="da745-119">Publisher.</span></span>

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

### <span data-ttu-id="da745-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="da745-120">-RolesAppliedTo</span></span>
<span data-ttu-id="da745-121">RolesAppliedTo.</span><span class="sxs-lookup"><span data-stu-id="da745-121">RolesAppliedTo.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da745-122">-Setting</span><span class="sxs-lookup"><span data-stu-id="da745-122">-Setting</span></span>
<span data-ttu-id="da745-123">Общедоступные параметры расширения.</span><span class="sxs-lookup"><span data-stu-id="da745-123">Public settings for the extension.</span></span>

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

### <span data-ttu-id="da745-124">-Type</span><span class="sxs-lookup"><span data-stu-id="da745-124">-Type</span></span>
<span data-ttu-id="da745-125">Введите.</span><span class="sxs-lookup"><span data-stu-id="da745-125">Type.</span></span>

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

### <span data-ttu-id="da745-126">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="da745-126">-TypeHandlerVersion</span></span>
<span data-ttu-id="da745-127">TypeHandlerVersion.</span><span class="sxs-lookup"><span data-stu-id="da745-127">TypeHandlerVersion.</span></span>

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

### <span data-ttu-id="da745-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da745-128">CommonParameters</span></span>
<span data-ttu-id="da745-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da745-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da745-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da745-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da745-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da745-131">INPUTS</span></span>

## <span data-ttu-id="da745-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da745-132">OUTPUTS</span></span>

### <span data-ttu-id="da745-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="da745-133">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="da745-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da745-134">NOTES</span></span>

<span data-ttu-id="da745-135">ALIASES</span><span class="sxs-lookup"><span data-stu-id="da745-135">ALIASES</span></span>

## <span data-ttu-id="da745-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da745-136">RELATED LINKS</span></span>

