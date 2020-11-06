---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagedApplication.md
ms.openlocfilehash: 953a810585550ec8895fc9306f78633beb4846a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559547"
---
# <span data-ttu-id="7309e-101">Get-AzureRmManagedApplication</span><span class="sxs-lookup"><span data-stu-id="7309e-101">Get-AzureRmManagedApplication</span></span>

## <span data-ttu-id="7309e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7309e-102">SYNOPSIS</span></span>
<span data-ttu-id="7309e-103">Получает управляемые приложения</span><span class="sxs-lookup"><span data-stu-id="7309e-103">Gets managed applications</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7309e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7309e-104">SYNTAX</span></span>

### <span data-ttu-id="7309e-105">Список всех наборов параметров управляемых приложений.</span><span class="sxs-lookup"><span data-stu-id="7309e-105">The list all managed applications parameter set.</span></span> <span data-ttu-id="7309e-106">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="7309e-106">(Default)</span></span>
```
Get-AzureRmManagedApplication [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7309e-107">Заданный параметр имени управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="7309e-107">The managed application name parameter set.</span></span>
```
Get-AzureRmManagedApplication [-Name <String>] -ResourceGroupName <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7309e-108">Заданный параметр идентификатора управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="7309e-108">The managed application Id parameter set.</span></span>
```
Get-AzureRmManagedApplication -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7309e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7309e-109">DESCRIPTION</span></span>
<span data-ttu-id="7309e-110">Командлет **Get-AzureRmManagedApplication** получает управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="7309e-110">The **Get-AzureRmManagedApplication** cmdlet gets managed applications</span></span>

## <span data-ttu-id="7309e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7309e-111">EXAMPLES</span></span>

### <span data-ttu-id="7309e-112">Пример 1: получение всех управляемых приложений в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="7309e-112">Example 1: Get all managed applications under a resource group</span></span>
```
PS C:\>Get-AzureRmManagedApplication -ResourceGroupName "MyRG"
```

<span data-ttu-id="7309e-113">Эта команда получает управляемые приложения в группе ресурсов "MyRG".</span><span class="sxs-lookup"><span data-stu-id="7309e-113">This command gets managed applications under resource group "MyRG"</span></span>

### <span data-ttu-id="7309e-114">Пример 2: получение всех управляемых приложений</span><span class="sxs-lookup"><span data-stu-id="7309e-114">Example 2: Get all managed applications</span></span>
```
PS C:\>Get-AzureRmManagedApplication
```

<span data-ttu-id="7309e-115">Эта команда получает все управляемые приложения в текущей подписке</span><span class="sxs-lookup"><span data-stu-id="7309e-115">This command get all managed applications under the current subscription</span></span>

## <span data-ttu-id="7309e-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7309e-116">PARAMETERS</span></span>

### <span data-ttu-id="7309e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7309e-117">-ApiVersion</span></span>
<span data-ttu-id="7309e-118">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7309e-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="7309e-119">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="7309e-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="7309e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7309e-120">-DefaultProfile</span></span>
<span data-ttu-id="7309e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7309e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7309e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="7309e-122">-Id</span></span>
<span data-ttu-id="7309e-123">Полный идентификатор управляемого приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="7309e-123">The fully qualified managed application Id, including the subscription.</span></span>
<span data-ttu-id="7309e-124">Например,/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span><span class="sxs-lookup"><span data-stu-id="7309e-124">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application Id parameter set.
Aliases: ResourceId, ManagedApplicationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7309e-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7309e-125">-Name</span></span>
<span data-ttu-id="7309e-126">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="7309e-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7309e-127">-Pre</span><span class="sxs-lookup"><span data-stu-id="7309e-127">-Pre</span></span>
<span data-ttu-id="7309e-128">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="7309e-128">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="7309e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7309e-129">-ResourceGroupName</span></span>
<span data-ttu-id="7309e-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7309e-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7309e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7309e-131">CommonParameters</span></span>
<span data-ttu-id="7309e-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7309e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7309e-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7309e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7309e-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7309e-134">INPUTS</span></span>

### <span data-ttu-id="7309e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7309e-135">System.String</span></span>

## <span data-ttu-id="7309e-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7309e-136">OUTPUTS</span></span>

### <span data-ttu-id="7309e-137">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="7309e-137">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="7309e-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="7309e-138">NOTES</span></span>

## <span data-ttu-id="7309e-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7309e-139">RELATED LINKS</span></span>

