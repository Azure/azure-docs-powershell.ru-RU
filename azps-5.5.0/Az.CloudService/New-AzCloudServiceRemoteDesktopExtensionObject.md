---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-azcloudserviceremotedesktopextensionobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRemoteDesktopExtensionObject.md
ms.openlocfilehash: 022093b8fe1df28a151405a18009b40dd24b0c97
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233489"
---
# <span data-ttu-id="bd4de-101">New-AzCloudServiceRemoteDesktopExtensionObject</span><span class="sxs-lookup"><span data-stu-id="bd4de-101">New-AzCloudServiceRemoteDesktopExtensionObject</span></span>

## <span data-ttu-id="bd4de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd4de-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4de-103">Создание объекта в памяти для расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="bd4de-103">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="bd4de-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd4de-104">SYNTAX</span></span>

```
New-AzCloudServiceRemoteDesktopExtensionObject [-Name] <String> [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-TypeHandlerVersion] <String>] [[-RolesAppliedTo] <String[]>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="bd4de-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd4de-105">DESCRIPTION</span></span>
<span data-ttu-id="bd4de-106">Создание объекта в памяти для расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="bd4de-106">Create a in-memory object for Remote Desktop Extension</span></span>

## <span data-ttu-id="bd4de-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd4de-107">EXAMPLES</span></span>

### <span data-ttu-id="bd4de-108">Пример 1. Создание объекта расширения удаленного рабочего стола</span><span class="sxs-lookup"><span data-stu-id="bd4de-108">Example 1: Create remote desktop extension object</span></span>
```powershell
PS C:\> $credential = Get-Credential
PS C:\> $expiration = (Get-Date).AddYears(1)
PS C:\> $extension = New-AzCloudServiceRemoteDesktopExtensionObject -Name 'RDPExtension' -Credential $credential -Expiration $expiration -TypeHandlerVersion '1.2.1'
```

<span data-ttu-id="bd4de-109">Эта команда создает объект расширения удаленного рабочего стола, который используется для создания или обновления облачной службы.</span><span class="sxs-lookup"><span data-stu-id="bd4de-109">This command creates remote desktop extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="bd4de-110">Дополнительные сведения см. в службе New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="bd4de-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="bd4de-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd4de-111">PARAMETERS</span></span>

### <span data-ttu-id="bd4de-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="bd4de-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="bd4de-113">Автоматическое обновление для незначительных версий.</span><span class="sxs-lookup"><span data-stu-id="bd4de-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="bd4de-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="bd4de-114">-Credential</span></span>
<span data-ttu-id="bd4de-115">Учетные данные для расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="bd4de-115">Credential for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="bd4de-116">-Expiration</span><span class="sxs-lookup"><span data-stu-id="bd4de-116">-Expiration</span></span>
<span data-ttu-id="bd4de-117">Окончание срока действия для расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="bd4de-117">Expiration for Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="bd4de-118">-Name</span><span class="sxs-lookup"><span data-stu-id="bd4de-118">-Name</span></span>
<span data-ttu-id="bd4de-119">Имя расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="bd4de-119">Name of Remote Desktop Extension.</span></span>

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

### <span data-ttu-id="bd4de-120">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="bd4de-120">-RolesAppliedTo</span></span>
<span data-ttu-id="bd4de-121">Применены роли.</span><span class="sxs-lookup"><span data-stu-id="bd4de-121">Roles applied to.</span></span>

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

### <span data-ttu-id="bd4de-122">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="bd4de-122">-TypeHandlerVersion</span></span>
<span data-ttu-id="bd4de-123">Версия расширения удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="bd4de-123">Remote Desktop Extension version.</span></span>

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

### <span data-ttu-id="bd4de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4de-124">CommonParameters</span></span>
<span data-ttu-id="bd4de-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd4de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4de-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd4de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4de-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd4de-127">INPUTS</span></span>

## <span data-ttu-id="bd4de-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd4de-128">OUTPUTS</span></span>

### <span data-ttu-id="bd4de-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="bd4de-129">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="bd4de-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd4de-130">NOTES</span></span>

<span data-ttu-id="bd4de-131">ALIASES</span><span class="sxs-lookup"><span data-stu-id="bd4de-131">ALIASES</span></span>

## <span data-ttu-id="bd4de-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd4de-132">RELATED LINKS</span></span>

