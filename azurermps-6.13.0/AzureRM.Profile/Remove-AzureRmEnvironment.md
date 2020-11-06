---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 05a4b2a475b2bd58de706ba038f2760d133b7dbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565805"
---
# <span data-ttu-id="a53fd-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a53fd-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="a53fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a53fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a53fd-103">Удаляет конечные точки и метаданные для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="a53fd-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a53fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a53fd-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a53fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a53fd-105">DESCRIPTION</span></span>
<span data-ttu-id="a53fd-106">Командлет Remove-AzureRmEnvironment удаляет конечные точки и сведения о метаданных для подключения к определенному экземпляру Azure.</span><span class="sxs-lookup"><span data-stu-id="a53fd-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="a53fd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a53fd-107">EXAMPLES</span></span>

### <span data-ttu-id="a53fd-108">Пример 1: создание и удаление тестовой среды</span><span class="sxs-lookup"><span data-stu-id="a53fd-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="a53fd-109">В этом примере показано, как создать среду с помощью Add-AzureRmEnvironment, а затем удалить среду с помощью Remove-AzureRmEnvironment.</span><span class="sxs-lookup"><span data-stu-id="a53fd-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="a53fd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a53fd-110">PARAMETERS</span></span>

### <span data-ttu-id="a53fd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a53fd-111">-DefaultProfile</span></span>
<span data-ttu-id="a53fd-112">Учетные данные, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a53fd-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a53fd-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a53fd-113">-Name</span></span>
<span data-ttu-id="a53fd-114">Указывает имя среды, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a53fd-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="a53fd-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="a53fd-115">-Scope</span></span>
<span data-ttu-id="a53fd-116">Определяет область изменений контекста, например, применяются ли изменения только к текущему процессу или ко всем сеансам, запускаемым этим пользователем.</span><span class="sxs-lookup"><span data-stu-id="a53fd-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a53fd-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a53fd-117">-Confirm</span></span>
<span data-ttu-id="a53fd-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a53fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a53fd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a53fd-119">-WhatIf</span></span>
<span data-ttu-id="a53fd-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a53fd-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a53fd-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a53fd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a53fd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a53fd-122">CommonParameters</span></span>
<span data-ttu-id="a53fd-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a53fd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a53fd-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a53fd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a53fd-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a53fd-125">INPUTS</span></span>

### <span data-ttu-id="a53fd-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a53fd-126">System.String</span></span>

## <span data-ttu-id="a53fd-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a53fd-127">OUTPUTS</span></span>

### <span data-ttu-id="a53fd-128">Microsoft. Azure. Commands. Profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a53fd-128">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a53fd-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a53fd-129">NOTES</span></span>

## <span data-ttu-id="a53fd-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a53fd-130">RELATED LINKS</span></span>

[<span data-ttu-id="a53fd-131">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a53fd-131">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="a53fd-132">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a53fd-132">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="a53fd-133">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a53fd-133">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

