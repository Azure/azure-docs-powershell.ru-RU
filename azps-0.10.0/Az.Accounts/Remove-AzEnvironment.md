---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/remove-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Remove-AzEnvironment.md
ms.openlocfilehash: fa16d5f534a0bb26c0976cbc75700f7390f62466
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909385"
---
# <span data-ttu-id="7e4cf-101">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e4cf-101">Remove-AzEnvironment</span></span>

## <span data-ttu-id="7e4cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="7e4cf-103">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="7e4cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e4cf-104">SYNTAX</span></span>

```
Remove-AzEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e4cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e4cf-105">DESCRIPTION</span></span>
<span data-ttu-id="7e4cf-106">Командлет Remove-AzEnvironment удаляет конечные точки и сведения о метаданных для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-106">The Remove-AzEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="7e4cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e4cf-107">EXAMPLES</span></span>

### <span data-ttu-id="7e4cf-108">Пример 1: создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="7e4cf-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="7e4cf-109">В этом примере показано, как создать среду с помощью Add-AzEnvironment, а затем удалить среду с помощью Remove-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-109">This example shows how to create an environment using Add-AzEnvironment, and then how to delete the environment using Remove-AzEnvironment.</span></span>

## <span data-ttu-id="7e4cf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e4cf-110">PARAMETERS</span></span>

### <span data-ttu-id="7e4cf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e4cf-111">-DefaultProfile</span></span>
<span data-ttu-id="7e4cf-112">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-112">The credentials, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e4cf-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e4cf-113">-Name</span></span>
<span data-ttu-id="7e4cf-114">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="7e4cf-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="7e4cf-115">-Scope</span></span>
<span data-ttu-id="7e4cf-116">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="7e4cf-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e4cf-117">-Confirm</span></span>
<span data-ttu-id="7e4cf-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e4cf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e4cf-119">-WhatIf</span></span>
<span data-ttu-id="7e4cf-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7e4cf-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e4cf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e4cf-122">CommonParameters</span></span>
<span data-ttu-id="7e4cf-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e4cf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e4cf-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7e4cf-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e4cf-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e4cf-125">INPUTS</span></span>

### <span data-ttu-id="7e4cf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7e4cf-126">System.String</span></span>

## <span data-ttu-id="7e4cf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e4cf-127">OUTPUTS</span></span>

### <span data-ttu-id="7e4cf-128">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e4cf-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="7e4cf-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e4cf-129">NOTES</span></span>

## <span data-ttu-id="7e4cf-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e4cf-130">RELATED LINKS</span></span>

[<span data-ttu-id="7e4cf-131">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e4cf-131">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="7e4cf-132">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e4cf-132">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="7e4cf-133">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="7e4cf-133">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

