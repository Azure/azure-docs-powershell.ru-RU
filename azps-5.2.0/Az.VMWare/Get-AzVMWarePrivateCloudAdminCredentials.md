---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325754"
---
# <span data-ttu-id="4511d-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="4511d-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="4511d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4511d-102">SYNOPSIS</span></span>
<span data-ttu-id="4511d-103">Укаймь учетных данных администратора для закрытого облака</span><span class="sxs-lookup"><span data-stu-id="4511d-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="4511d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4511d-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4511d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4511d-105">DESCRIPTION</span></span>
<span data-ttu-id="4511d-106">Укаймь учетных данных администратора для закрытого облака</span><span class="sxs-lookup"><span data-stu-id="4511d-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="4511d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4511d-107">EXAMPLES</span></span>

### <span data-ttu-id="4511d-108">Пример 1. Получите учетные данные администратора закрытого облака</span><span class="sxs-lookup"><span data-stu-id="4511d-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="4511d-109">Получить учетные данные администратора частного облака</span><span class="sxs-lookup"><span data-stu-id="4511d-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="4511d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4511d-110">PARAMETERS</span></span>

### <span data-ttu-id="4511d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4511d-111">-DefaultProfile</span></span>
<span data-ttu-id="4511d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4511d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4511d-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="4511d-113">-PrivateCloudName</span></span>
<span data-ttu-id="4511d-114">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="4511d-114">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4511d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4511d-115">-ResourceGroupName</span></span>
<span data-ttu-id="4511d-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4511d-116">The name of the resource group.</span></span>
<span data-ttu-id="4511d-117">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="4511d-117">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4511d-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4511d-118">-SubscriptionId</span></span>
<span data-ttu-id="4511d-119">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="4511d-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4511d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4511d-120">-Confirm</span></span>
<span data-ttu-id="4511d-121">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4511d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4511d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4511d-122">-WhatIf</span></span>
<span data-ttu-id="4511d-123">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4511d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4511d-124">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4511d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4511d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4511d-125">CommonParameters</span></span>
<span data-ttu-id="4511d-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4511d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4511d-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4511d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4511d-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4511d-128">INPUTS</span></span>

## <span data-ttu-id="4511d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4511d-129">OUTPUTS</span></span>

### <span data-ttu-id="4511d-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="4511d-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="4511d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4511d-131">NOTES</span></span>

<span data-ttu-id="4511d-132">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4511d-132">ALIASES</span></span>

## <span data-ttu-id="4511d-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4511d-133">RELATED LINKS</span></span>

