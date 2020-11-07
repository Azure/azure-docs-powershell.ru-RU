---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesAccount.md
ms.openlocfilehash: dbe206a744cc0a80d166d93b09ff0ab000cb3bc6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730785"
---
# <span data-ttu-id="dcfb8-101">Get-AzNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dcfb8-101">Get-AzNetAppFilesAccount</span></span>

## <span data-ttu-id="dcfb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dcfb8-102">SYNOPSIS</span></span>
<span data-ttu-id="dcfb8-103">Получение сведений о учетной записи NetApp файлов Azure (ANF).</span><span class="sxs-lookup"><span data-stu-id="dcfb8-103">Gets details of an Azure NetApp Files (ANF) account.</span></span>

## <span data-ttu-id="dcfb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dcfb8-104">SYNTAX</span></span>

### <span data-ttu-id="dcfb8-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcfb8-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesAccount -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcfb8-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dcfb8-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesAccount -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcfb8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcfb8-107">DESCRIPTION</span></span>
<span data-ttu-id="dcfb8-108">Командлет **Get-AzNetAppFilesAccount** получает сведения о учетной записи ANF.</span><span class="sxs-lookup"><span data-stu-id="dcfb8-108">The **Get-AzNetAppFilesAccount** cmdlet gets details of an ANF account.</span></span>

## <span data-ttu-id="dcfb8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dcfb8-109">EXAMPLES</span></span>

### <span data-ttu-id="dcfb8-110">Пример 1: получение учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dcfb8-110">Example 1: Get an ANF account</span></span>
```
PS C:\>Get-AzNetAppFilesAccount -ResourceGroupName "MyRG" -Name "MyAnfAccount"

Output:

Location          : westus2
Id                : /subscriptions/mySubs/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount
Name              : MyAnfAccount
Type              : Microsoft.NetApp/netAppAccounts
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="dcfb8-111">Эта команда получает учетную запись с именем MyAnfAccount.</span><span class="sxs-lookup"><span data-stu-id="dcfb8-111">This command gets the account named MyAnfAccount.</span></span>

## <span data-ttu-id="dcfb8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dcfb8-112">PARAMETERS</span></span>

### <span data-ttu-id="dcfb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcfb8-113">-DefaultProfile</span></span>
<span data-ttu-id="dcfb8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcfb8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcfb8-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="dcfb8-115">-Name</span></span>
<span data-ttu-id="dcfb8-116">Имя учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dcfb8-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: AccountName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcfb8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcfb8-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcfb8-118">Группа ресурсов для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dcfb8-118">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="dcfb8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dcfb8-119">-ResourceId</span></span>
<span data-ttu-id="dcfb8-120">Идентификатор ресурса для учетной записи ANF</span><span class="sxs-lookup"><span data-stu-id="dcfb8-120">The resource id of the ANF account</span></span>

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

### <span data-ttu-id="dcfb8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcfb8-121">CommonParameters</span></span>
<span data-ttu-id="dcfb8-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dcfb8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="dcfb8-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcfb8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcfb8-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dcfb8-124">INPUTS</span></span>

### <span data-ttu-id="dcfb8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="dcfb8-125">System.String</span></span>

## <span data-ttu-id="dcfb8-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcfb8-126">OUTPUTS</span></span>

### <span data-ttu-id="dcfb8-127">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="dcfb8-127">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="dcfb8-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="dcfb8-128">NOTES</span></span>

## <span data-ttu-id="dcfb8-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcfb8-129">RELATED LINKS</span></span>
