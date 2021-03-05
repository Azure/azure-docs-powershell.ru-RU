---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 5ae7383f71524c87518b9f48cbb314bf74de633e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998217"
---
# <span data-ttu-id="2257a-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="2257a-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="2257a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2257a-102">SYNOPSIS</span></span>
<span data-ttu-id="2257a-103">Создание объекта в памяти для расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2257a-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="2257a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2257a-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="2257a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2257a-105">DESCRIPTION</span></span>
<span data-ttu-id="2257a-106">Создание объекта в памяти для расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2257a-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="2257a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2257a-107">EXAMPLES</span></span>

### <span data-ttu-id="2257a-108">Пример 1. Создание объекта расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="2257a-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="2257a-109">Эта команда создает объект расширения удаленного рабочего стола, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="2257a-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="2257a-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="2257a-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="2257a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2257a-111">PARAMETERS</span></span>

### <span data-ttu-id="2257a-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2257a-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="2257a-113">Автоматическое обновление для незначительных версий.</span><span class="sxs-lookup"><span data-stu-id="2257a-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="2257a-114">-Credential</span></span>
<span data-ttu-id="2257a-115">Учетные данные для расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2257a-115">Credential for Remote Desktop Extension.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="2257a-116">-Expiration</span></span>
<span data-ttu-id="2257a-117">Окончание срока действия для расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2257a-117">Expiration for Remote Desktop Extension.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="2257a-118">-Name</span></span>
<span data-ttu-id="2257a-119">Имя расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2257a-119">Name of Remote Desktop Extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="2257a-120">-RolesAppliedTo</span></span>
<span data-ttu-id="2257a-121">Применены роли.</span><span class="sxs-lookup"><span data-stu-id="2257a-121">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2257a-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="2257a-123">Версия расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2257a-123">Remote Desktop Extension version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2257a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2257a-124">CommonParameters</span></span>
<span data-ttu-id="2257a-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2257a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2257a-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2257a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2257a-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2257a-127">INPUTS</span></span>

## <span data-ttu-id="2257a-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2257a-128">OUTPUTS</span></span>

### <span data-ttu-id="2257a-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="2257a-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="2257a-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2257a-130">NOTES</span></span>

<span data-ttu-id="2257a-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2257a-131">ALIASES</span></span>

## <span data-ttu-id="2257a-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2257a-132">RELATED LINKS</span></span>

