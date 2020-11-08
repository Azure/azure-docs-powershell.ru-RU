---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 777c3dd8214288a3f7c5b5be92a65260bf8c6c98
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079683"
---
# <span data-ttu-id="23ca8-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="23ca8-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="23ca8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23ca8-102">SYNOPSIS</span></span>
<span data-ttu-id="23ca8-103">Получение сведений о записях общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="23ca8-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="23ca8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23ca8-104">SYNTAX</span></span>

### <span data-ttu-id="23ca8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23ca8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23ca8-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ca8-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23ca8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23ca8-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23ca8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ca8-108">DESCRIPTION</span></span>
<span data-ttu-id="23ca8-109">Командлет **Get-AzDataShareAccount** получает сведения об учетных записях для общего доступа к данным в подписке или группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="23ca8-110">Если вы задаете имя учетной записи, этот командлет получает сведения об этой учетной записи datshare.</span><span class="sxs-lookup"><span data-stu-id="23ca8-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="23ca8-111">Если имя не задано, этот командлет получает сведения обо всех учетных записях данных для общего доступа в группе подписку или ресурсах Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="23ca8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23ca8-112">EXAMPLES</span></span>

### <span data-ttu-id="23ca8-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23ca8-113">Example 1</span></span>
```
PS C:\> Get-AzDataShareAccount -ResourceGroupName "ADS"
DataShareAccountName    : WikiADS
ResourceGroupName       : ADS
Location                : WestUS
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
DataShareAccountName    : WikiADS2
ResourceGroupName       : ADS
Location                : westus
ProvisioningState       : Succeeded
Tags                    : {}
Identity                : Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSIdentity
Type                    : Microsoft.DataShare/accounts
Id                      : /subscriptions/4834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiADS
```

<span data-ttu-id="23ca8-114">Эта команда отображает сведения обо всех учетных записях для общего доступа в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="23ca8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23ca8-115">PARAMETERS</span></span>

### <span data-ttu-id="23ca8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ca8-116">-DefaultProfile</span></span>
<span data-ttu-id="23ca8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ca8-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23ca8-118">-Name</span></span>
<span data-ttu-id="23ca8-119">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-119">Azure data share account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ca8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ca8-120">-ResourceGroupName</span></span>
<span data-ttu-id="23ca8-121">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-121">The resource group name of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ca8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23ca8-122">-ResourceId</span></span>
<span data-ttu-id="23ca8-123">Идентификатор ресурса учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="23ca8-123">The resource id of the azure data share account.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23ca8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ca8-124">CommonParameters</span></span>
<span data-ttu-id="23ca8-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23ca8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ca8-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23ca8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ca8-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23ca8-127">INPUTS</span></span>

### <span data-ttu-id="23ca8-128">System. String</span><span class="sxs-lookup"><span data-stu-id="23ca8-128">System.String</span></span>

## <span data-ttu-id="23ca8-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ca8-129">OUTPUTS</span></span>

### <span data-ttu-id="23ca8-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="23ca8-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="23ca8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="23ca8-131">NOTES</span></span>

## <span data-ttu-id="23ca8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ca8-132">RELATED LINKS</span></span>
