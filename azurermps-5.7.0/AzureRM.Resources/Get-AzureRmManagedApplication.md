---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 3dd86c186d05ce59f237be51b8e059e800c47a84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733234"
---
# <span data-ttu-id="839b1-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="839b1-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="839b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="839b1-102">SYNOPSIS</span></span>
<span data-ttu-id="839b1-103">Получает управляемые приложения</span><span class="sxs-lookup"><span data-stu-id="839b1-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="839b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="839b1-104">SYNTAX</span></span>

### <span data-ttu-id="839b1-105">GetBySubscription (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="839b1-105">GetBySubscription (Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="839b1-106">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="839b1-106">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="839b1-107">GetById</span><span class="sxs-lookup"><span data-stu-id="839b1-107">GetById</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="839b1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="839b1-108">DESCRIPTION</span></span>
<span data-ttu-id="839b1-109">Командлет **Get-AzureRmManagedApplication** получает управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="839b1-109">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="839b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="839b1-110">EXAMPLES</span></span>

### <span data-ttu-id="839b1-111">Пример 1: получение всех управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="839b1-111">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="839b1-112">Эта команда получает управляемые приложения в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="839b1-112">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="839b1-113">Пример 2: получение всех управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="839b1-113">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="839b1-114">Эта команда получает все управляемые приложения в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="839b1-114">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="839b1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="839b1-115">PARAMETERS</span></span>

### <span data-ttu-id="839b1-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="839b1-116">-ApiVersion</span></span>
<span data-ttu-id="839b1-117">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="839b1-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="839b1-118">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="839b1-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="839b1-119">-DefaultProfile</span></span>
<span data-ttu-id="839b1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="839b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-121">-ID</span><span class="sxs-lookup"><span data-stu-id="839b1-121">-Id</span></span>
<span data-ttu-id="839b1-122">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="839b1-122">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="839b1-123">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="839b1-123">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: String
Parameter Sets: GetById
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="839b1-124">-Name</span></span>
<span data-ttu-id="839b1-125">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="839b1-125">The managed application name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="839b1-126">-Pre</span></span>
<span data-ttu-id="839b1-127">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="839b1-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="839b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="839b1-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="839b1-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="839b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="839b1-130">CommonParameters</span></span>
<span data-ttu-id="839b1-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="839b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="839b1-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="839b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="839b1-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="839b1-133">INPUTS</span></span>

### <span data-ttu-id="839b1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="839b1-134">System.String</span></span>

## <span data-ttu-id="839b1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="839b1-135">OUTPUTS</span></span>

### <span data-ttu-id="839b1-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="839b1-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="839b1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="839b1-137">NOTES</span></span>

## <span data-ttu-id="839b1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="839b1-138">RELATED LINKS</span></span>
