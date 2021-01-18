---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: 2c7ba44358db4e6a578f9876e26a099b2242badc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507016"
---
# <span data-ttu-id="36889-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="36889-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="36889-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36889-102">SYNOPSIS</span></span>
<span data-ttu-id="36889-103">Удаляет конечные точки и метаданные для подключения к экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="36889-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="36889-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36889-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36889-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36889-105">DESCRIPTION</span></span>
<span data-ttu-id="36889-106">Новый Remove-AzEnvironment удаляет конечные точки и метаданные для подключения к экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="36889-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="36889-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36889-107">EXAMPLES</span></span>

### <span data-ttu-id="36889-108">Пример 1. Создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="36889-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="36889-109">В этом примере показано, как создать среду с помощью Add-AzEnvironment и как удалить ее с помощью Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="36889-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="36889-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36889-110">PARAMETERS</span></span>

### <span data-ttu-id="36889-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36889-111">-DefaultProfile</span></span>
<span data-ttu-id="36889-112">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36889-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36889-113">-Name</span><span class="sxs-lookup"><span data-stu-id="36889-113">-Name</span></span>
<span data-ttu-id="36889-114">Указывает имя среды, которая будет удаляться.</span><span class="sxs-lookup"><span data-stu-id="36889-114">Specifies the name of the environment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36889-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="36889-115">-Scope</span></span>
<span data-ttu-id="36889-116">Определяет область изменения контекста, например, применяются ли изменения только к текущему процессу или же к всем сеансам, на которые начал пользователь.</span><span class="sxs-lookup"><span data-stu-id="36889-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36889-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36889-117">-Confirm</span></span>
<span data-ttu-id="36889-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36889-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36889-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36889-119">-WhatIf</span></span>
<span data-ttu-id="36889-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36889-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36889-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36889-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36889-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36889-122">CommonParameters</span></span>
<span data-ttu-id="36889-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36889-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36889-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36889-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36889-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36889-125">INPUTS</span></span>

### <span data-ttu-id="36889-126">System.String</span><span class="sxs-lookup"><span data-stu-id="36889-126">System.String</span></span>

## <span data-ttu-id="36889-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36889-127">OUTPUTS</span></span>

### <span data-ttu-id="36889-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="36889-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="36889-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36889-129">NOTES</span></span>

## <span data-ttu-id="36889-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36889-130">RELATED LINKS</span></span>

[<span data-ttu-id="36889-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="36889-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="36889-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="36889-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="36889-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="36889-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

