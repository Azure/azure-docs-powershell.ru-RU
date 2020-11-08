---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 257421a43c3da11c82316eaf58d2983fe47d5f05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078961"
---
# <span data-ttu-id="bfc24-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="bfc24-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="bfc24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bfc24-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc24-103">Получение сведений о пуле файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="bfc24-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="bfc24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bfc24-104">SYNTAX</span></span>

### <span data-ttu-id="bfc24-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bfc24-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc24-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc24-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bfc24-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfc24-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfc24-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc24-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc24-109">Командлет **Get-AzNetAppFilesPool** получает сведения о пуле ANF.</span><span class="sxs-lookup"><span data-stu-id="bfc24-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="bfc24-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bfc24-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc24-111">Пример 1: получение пула ANF</span><span class="sxs-lookup"><span data-stu-id="bfc24-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="bfc24-112">Эта команда получает учетную запись с именем MyAnfPool из учетной записи "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="bfc24-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="bfc24-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bfc24-113">PARAMETERS</span></span>

### <span data-ttu-id="bfc24-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="bfc24-114">-AccountName</span></span>
<span data-ttu-id="bfc24-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="bfc24-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc24-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="bfc24-116">-AccountObject</span></span>
<span data-ttu-id="bfc24-117">Объект Account, содержащий пул, который нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="bfc24-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfc24-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc24-118">-DefaultProfile</span></span>
<span data-ttu-id="bfc24-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bfc24-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfc24-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bfc24-120">-Name</span></span>
<span data-ttu-id="bfc24-121">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="bfc24-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc24-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc24-122">-ResourceGroupName</span></span>
<span data-ttu-id="bfc24-123">Группа ресурсов в пуле ANF</span><span class="sxs-lookup"><span data-stu-id="bfc24-123">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfc24-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfc24-124">-ResourceId</span></span>
<span data-ttu-id="bfc24-125">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="bfc24-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="bfc24-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc24-126">CommonParameters</span></span>
<span data-ttu-id="bfc24-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bfc24-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc24-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bfc24-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc24-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bfc24-129">INPUTS</span></span>

### <span data-ttu-id="bfc24-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bfc24-130">System.String</span></span>

### <span data-ttu-id="bfc24-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="bfc24-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="bfc24-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bfc24-132">OUTPUTS</span></span>

### <span data-ttu-id="bfc24-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="bfc24-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="bfc24-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="bfc24-134">NOTES</span></span>

## <span data-ttu-id="bfc24-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bfc24-135">RELATED LINKS</span></span>