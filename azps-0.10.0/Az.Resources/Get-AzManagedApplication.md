---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzManagedApplication.md
ms.openlocfilehash: c9a0c55a55990fc14b86783cab003e058a1111fc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910949"
---
# <span data-ttu-id="1a51e-101">Get-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="1a51e-101">Get-AzManagedApplication</span></span>

## <span data-ttu-id="1a51e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a51e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a51e-103">Получает управляемые приложения</span><span class="sxs-lookup"><span data-stu-id="1a51e-103">Gets managed applications</span></span>

## <span data-ttu-id="1a51e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a51e-104">SYNTAX</span></span>

### <span data-ttu-id="1a51e-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a51e-105">GetBySubscription (Default)</span></span>
```
Get-AzManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a51e-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a51e-106">GetByNameAndResourceGroup</span></span>
```
Get-AzManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a51e-107">GetById</span><span class="sxs-lookup"><span data-stu-id="1a51e-107">GetById</span></span>
```
Get-AzManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a51e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a51e-108">DESCRIPTION</span></span>
<span data-ttu-id="1a51e-109">Командлет **Get-AzManagedApplication** получает управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="1a51e-109">The **Get-AzManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="1a51e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a51e-110">EXAMPLES</span></span>

### <span data-ttu-id="1a51e-111">Пример 1: получение всех управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="1a51e-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="1a51e-112">Эта команда получает управляемые приложения в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="1a51e-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="1a51e-113">Пример 2: получение всех управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="1a51e-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzManagedApplication
```

<span data-ttu-id="1a51e-114">Эта команда получает все управляемые приложения в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="1a51e-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="1a51e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a51e-115">PARAMETERS</span></span>

### <span data-ttu-id="1a51e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1a51e-116">-ApiVersion</span></span>
<span data-ttu-id="1a51e-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a51e-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="1a51e-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="1a51e-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="1a51e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a51e-119">-DefaultProfile</span></span>
<span data-ttu-id="1a51e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a51e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a51e-121">-ID</span><span class="sxs-lookup"><span data-stu-id="1a51e-121">-Id</span></span>
<span data-ttu-id="1a51e-122">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="1a51e-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="1a51e-123">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="1a51e-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a51e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a51e-124">-Name</span></span>
<span data-ttu-id="1a51e-125">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="1a51e-125">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a51e-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="1a51e-126">-Pre</span></span>
<span data-ttu-id="1a51e-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="1a51e-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1a51e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a51e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1a51e-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a51e-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a51e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a51e-130">CommonParameters</span></span>
<span data-ttu-id="1a51e-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a51e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a51e-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a51e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a51e-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a51e-133">INPUTS</span></span>

### <span data-ttu-id="1a51e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1a51e-134">System.String</span></span>

## <span data-ttu-id="1a51e-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a51e-135">OUTPUTS</span></span>

### <span data-ttu-id="1a51e-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1a51e-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1a51e-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a51e-137">NOTES</span></span>

## <span data-ttu-id="1a51e-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a51e-138">RELATED LINKS</span></span>
