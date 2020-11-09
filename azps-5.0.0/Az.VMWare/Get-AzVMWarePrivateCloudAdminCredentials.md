---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/get-azvmwareprivatecloudadmincredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Get-AzVMWarePrivateCloudAdminCredentials.md
ms.openlocfilehash: 64552dada33249779e474dc72063f828c9336ffd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248438"
---
# <span data-ttu-id="2ae6f-101">Get-AzVMWarePrivateCloudAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="2ae6f-101">Get-AzVMWarePrivateCloudAdminCredentials</span></span>

## <span data-ttu-id="2ae6f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ae6f-102">SYNOPSIS</span></span>
<span data-ttu-id="2ae6f-103">Список учетных данных администратора для частного облака</span><span class="sxs-lookup"><span data-stu-id="2ae6f-103">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="2ae6f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ae6f-104">SYNTAX</span></span>

```
Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2ae6f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-105">DESCRIPTION</span></span>
<span data-ttu-id="2ae6f-106">Список учетных данных администратора для частного облака</span><span class="sxs-lookup"><span data-stu-id="2ae6f-106">List the admin credentials for the private cloud</span></span>

## <span data-ttu-id="2ae6f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-107">EXAMPLES</span></span>

### <span data-ttu-id="2ae6f-108">Пример 1: получение учетных данных администратора частного облака</span><span class="sxs-lookup"><span data-stu-id="2ae6f-108">Example 1: Get admin credential of private cloud</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloudAdminCredentials -PrivateCloudName azps-test-cloud -ResourceGroupName azps-test-group

NsxtPassword NsxtUsername VcenterPassword VcenterUsername
------------ ------------ --------------- ---------------
************ admin        ************    cloudadmin@vsphere.local
```

<span data-ttu-id="2ae6f-109">Получение учетных данных администратора частного облака</span><span class="sxs-lookup"><span data-stu-id="2ae6f-109">Get admin credential of private cloud</span></span>

## <span data-ttu-id="2ae6f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-110">PARAMETERS</span></span>

### <span data-ttu-id="2ae6f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ae6f-111">-DefaultProfile</span></span>
<span data-ttu-id="2ae6f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ae6f-113">-PrivateCloudName</span><span class="sxs-lookup"><span data-stu-id="2ae6f-113">-PrivateCloudName</span></span>
<span data-ttu-id="2ae6f-114">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="2ae6f-114">Name of the private cloud</span></span>

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

### <span data-ttu-id="2ae6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ae6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="2ae6f-116">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-116">The name of the resource group.</span></span>
<span data-ttu-id="2ae6f-117">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-117">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2ae6f-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2ae6f-118">-SubscriptionId</span></span>
<span data-ttu-id="2ae6f-119">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-119">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="2ae6f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ae6f-120">-Confirm</span></span>
<span data-ttu-id="2ae6f-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ae6f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ae6f-122">-WhatIf</span></span>
<span data-ttu-id="2ae6f-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ae6f-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ae6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ae6f-125">CommonParameters</span></span>
<span data-ttu-id="2ae6f-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ae6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ae6f-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ae6f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ae6f-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ae6f-128">INPUTS</span></span>

## <span data-ttu-id="2ae6f-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-129">OUTPUTS</span></span>

### <span data-ttu-id="2ae6f-130">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IAdminCredentials</span><span class="sxs-lookup"><span data-stu-id="2ae6f-130">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IAdminCredentials</span></span>

## <span data-ttu-id="2ae6f-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ae6f-131">NOTES</span></span>

<span data-ttu-id="2ae6f-132">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-132">ALIASES</span></span>

## <span data-ttu-id="2ae6f-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ae6f-133">RELATED LINKS</span></span>
