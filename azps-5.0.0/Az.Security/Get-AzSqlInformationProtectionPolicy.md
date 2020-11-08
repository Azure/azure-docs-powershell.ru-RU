---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSqlInformationProtectionPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSqlInformationProtectionPolicy.md
ms.openlocfilehash: 7f84c3b10577eea0d035c2ce84b3aa8a61af4a3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246197"
---
# <span data-ttu-id="36057-101">Get-AzSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36057-101">Get-AzSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="36057-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36057-102">SYNOPSIS</span></span>
<span data-ttu-id="36057-103">Получение действующей политики защиты данных SQL для клиента.</span><span class="sxs-lookup"><span data-stu-id="36057-103">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="36057-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36057-104">SYNTAX</span></span>

```
Get-AzSqlInformationProtectionPolicy [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36057-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36057-105">DESCRIPTION</span></span>
<span data-ttu-id="36057-106">Получение действующей политики защиты данных SQL для клиента.</span><span class="sxs-lookup"><span data-stu-id="36057-106">Retrieves the effective tenant SQL information protection policy.</span></span>

## <span data-ttu-id="36057-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36057-107">EXAMPLES</span></span>

### <span data-ttu-id="36057-108">Образом</span><span class="sxs-lookup"><span data-stu-id="36057-108">Example</span></span>
```powershell
PS C:\> Get-AzSqlInformationProtectionPolicy
```

## <span data-ttu-id="36057-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36057-109">PARAMETERS</span></span>

### <span data-ttu-id="36057-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36057-110">-AsJob</span></span>
<span data-ttu-id="36057-111">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="36057-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36057-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36057-112">-DefaultProfile</span></span>
<span data-ttu-id="36057-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36057-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36057-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36057-114">CommonParameters</span></span>
<span data-ttu-id="36057-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36057-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36057-116">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36057-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36057-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36057-117">INPUTS</span></span>

### <span data-ttu-id="36057-118">System. String</span><span class="sxs-lookup"><span data-stu-id="36057-118">System.string</span></span>

## <span data-ttu-id="36057-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36057-119">OUTPUTS</span></span>

### <span data-ttu-id="36057-120">Microsoft. Azure. Commands. SecurityCenter. Models. SqlInformationProtectionPolicy. PSSqlInformationProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="36057-120">Microsoft.Azure.Commands.SecurityCenter.Models.SqlInformationProtectionPolicy.PSSqlInformationProtectionPolicy</span></span>

## <span data-ttu-id="36057-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="36057-121">NOTES</span></span>

## <span data-ttu-id="36057-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36057-122">RELATED LINKS</span></span>
