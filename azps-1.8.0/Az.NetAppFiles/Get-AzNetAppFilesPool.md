---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 8a85f3dff99184be984a7b08c7a4cafe25c697d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730782"
---
# <span data-ttu-id="a9ac4-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a9ac4-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="a9ac4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a9ac4-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ac4-103">Получение сведений о пуле файлов Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="a9ac4-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="a9ac4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a9ac4-104">SYNTAX</span></span>

### <span data-ttu-id="a9ac4-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a9ac4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ac4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9ac4-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ac4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9ac4-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9ac4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9ac4-108">DESCRIPTION</span></span>
<span data-ttu-id="a9ac4-109">Командлет **Get-AzNetAppFilesPool** получает сведения о пуле ANF.</span><span class="sxs-lookup"><span data-stu-id="a9ac4-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="a9ac4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a9ac4-110">EXAMPLES</span></span>

### <span data-ttu-id="a9ac4-111">Пример 1: получение пула ANF</span><span class="sxs-lookup"><span data-stu-id="a9ac4-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="a9ac4-112">Эта команда получает учетную запись с именем MyAnfPool из учетной записи "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="a9ac4-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="a9ac4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a9ac4-113">PARAMETERS</span></span>

### <span data-ttu-id="a9ac4-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="a9ac4-114">-AccountName</span></span>
<span data-ttu-id="a9ac4-115">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="a9ac4-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="a9ac4-116">-AccountObject</span></span>
<span data-ttu-id="a9ac4-117">Объект Account, содержащий пул, который нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="a9ac4-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ac4-118">-DefaultProfile</span></span>
<span data-ttu-id="a9ac4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a9ac4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a9ac4-120">-Name</span></span>
<span data-ttu-id="a9ac4-121">Название пула ANF</span><span class="sxs-lookup"><span data-stu-id="a9ac4-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ac4-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9ac4-123">Группа ресурсов в пуле ANF</span><span class="sxs-lookup"><span data-stu-id="a9ac4-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ac4-124">-ResourceId</span></span>
<span data-ttu-id="a9ac4-125">Идентификатор ресурса пула ANF</span><span class="sxs-lookup"><span data-stu-id="a9ac4-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9ac4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ac4-126">CommonParameters</span></span>
<span data-ttu-id="a9ac4-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a9ac4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a9ac4-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ac4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ac4-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a9ac4-129">INPUTS</span></span>

### <span data-ttu-id="a9ac4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ac4-130">System.String</span></span>

### <span data-ttu-id="a9ac4-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="a9ac4-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="a9ac4-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a9ac4-132">OUTPUTS</span></span>

### <span data-ttu-id="a9ac4-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a9ac4-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a9ac4-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="a9ac4-134">NOTES</span></span>

## <span data-ttu-id="a9ac4-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a9ac4-135">RELATED LINKS</span></span>
