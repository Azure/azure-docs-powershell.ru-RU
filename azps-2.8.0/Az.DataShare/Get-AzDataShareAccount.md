---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashareaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareAccount.md
ms.openlocfilehash: 68a9c47f3d5f5313a84729d0a7e0cdd5a2c3fac4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721213"
---
# <span data-ttu-id="6dfb2-101">Get-AzDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="6dfb2-101">Get-AzDataShareAccount</span></span>

## <span data-ttu-id="6dfb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6dfb2-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfb2-103">Получение сведений о записях общего доступа к данным</span><span class="sxs-lookup"><span data-stu-id="6dfb2-103">Gets information about DataShare Accounts</span></span>

## <span data-ttu-id="6dfb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6dfb2-104">SYNTAX</span></span>

### <span data-ttu-id="6dfb2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6dfb2-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dfb2-106">ByResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfb2-106">ByResourceGroupParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfb2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfb2-107">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6dfb2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dfb2-108">DESCRIPTION</span></span>
<span data-ttu-id="6dfb2-109">Командлет **Get-AzDataShareAccount** получает сведения об учетных записях для общего доступа к данным в подписке или группе ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-109">The **Get-AzDataShareAccount** cmdlet gets information about datashare accounts in an Azure subscription / resource group.</span></span>
<span data-ttu-id="6dfb2-110">Если вы задаете имя учетной записи, этот командлет получает сведения об этой учетной записи datshare.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-110">If you specify the name of an account, this cmdlet gets information about that datshare account.</span></span>
<span data-ttu-id="6dfb2-111">Если имя не задано, этот командлет получает сведения обо всех учетных записях данных для общего доступа в группе подписку или ресурсах Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-111">If you do not specify a name, this cmdlet gets information about all of the datashare accounts in an Azure subscription / resource group.</span></span>

## <span data-ttu-id="6dfb2-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6dfb2-112">EXAMPLES</span></span>

### <span data-ttu-id="6dfb2-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6dfb2-113">Example 1</span></span>
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

<span data-ttu-id="6dfb2-114">Эта команда отображает сведения обо всех учетных записях для общего доступа в подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-114">This command displays information about all datashare accounts in the Azure subscription.</span></span>

## <span data-ttu-id="6dfb2-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6dfb2-115">PARAMETERS</span></span>

### <span data-ttu-id="6dfb2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfb2-116">-DefaultProfile</span></span>
<span data-ttu-id="6dfb2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfb2-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6dfb2-118">-Name</span></span>
<span data-ttu-id="6dfb2-119">Имя учетной записи для предоставления доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-119">Azure data share account name.</span></span>

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

### <span data-ttu-id="6dfb2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfb2-120">-ResourceGroupName</span></span>
<span data-ttu-id="6dfb2-121">Имя группы ресурсов для учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-121">The resource group name of the azure data share account.</span></span>

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

### <span data-ttu-id="6dfb2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6dfb2-122">-ResourceId</span></span>
<span data-ttu-id="6dfb2-123">Идентификатор ресурса учетной записи общего доступа к данным Azure.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-123">The resource id of the azure data share account.</span></span>

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

### <span data-ttu-id="6dfb2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfb2-124">CommonParameters</span></span>
<span data-ttu-id="6dfb2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6dfb2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfb2-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dfb2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfb2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6dfb2-127">INPUTS</span></span>

### <span data-ttu-id="6dfb2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6dfb2-128">System.String</span></span>

## <span data-ttu-id="6dfb2-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6dfb2-129">OUTPUTS</span></span>

### <span data-ttu-id="6dfb2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span><span class="sxs-lookup"><span data-stu-id="6dfb2-130">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareAccount</span></span>

## <span data-ttu-id="6dfb2-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="6dfb2-131">NOTES</span></span>

## <span data-ttu-id="6dfb2-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6dfb2-132">RELATED LINKS</span></span>
