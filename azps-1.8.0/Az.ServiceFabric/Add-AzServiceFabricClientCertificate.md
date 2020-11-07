---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: bb6280eb623f52256eda5324e3d7980894fc91e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729128"
---
# <span data-ttu-id="90f83-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="90f83-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="90f83-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90f83-102">SYNOPSIS</span></span>
<span data-ttu-id="90f83-103">Добавьте в кластер общее имя или отпечаток для целей проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="90f83-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="90f83-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90f83-104">SYNTAX</span></span>

### <span data-ttu-id="90f83-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="90f83-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f83-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="90f83-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f83-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="90f83-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90f83-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="90f83-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f83-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90f83-109">DESCRIPTION</span></span>
<span data-ttu-id="90f83-110">С помощью **Add-AzServiceFabricClientCertificate** добавьте в кластер общего имени и отпечаток поставщика или отпечаток сертификата, чтобы клиент мог использовать его для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="90f83-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="90f83-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90f83-111">EXAMPLES</span></span>

### <span data-ttu-id="90f83-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="90f83-112">Example 1</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="90f83-113">Эта команда добавит сертификат с отпечатком "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер, чтобы клиент мог использовать этот сертификат в качестве администратора для связи с кластером.</span><span class="sxs-lookup"><span data-stu-id="90f83-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="90f83-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="90f83-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="90f83-115">Эта команда добавит сертификат клиента только для чтения с общим именем "Contoso.com", а отпечаток поставщика — "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A" в кластер.</span><span class="sxs-lookup"><span data-stu-id="90f83-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="90f83-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90f83-116">PARAMETERS</span></span>

### <span data-ttu-id="90f83-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="90f83-117">-Admin</span></span>
<span data-ttu-id="90f83-118">Тип проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="90f83-118">Client authentication type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="90f83-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="90f83-120">Укажите отпечаток сертификата клиента, у которого есть разрешение администратора.</span><span class="sxs-lookup"><span data-stu-id="90f83-120">Specify client certificate thumbprint that only has admin permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="90f83-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="90f83-122">Укажите общее имя клиента, отпечаток поставщика и тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="90f83-122">Specify client common name, issuer thumbprint, and authentication type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="90f83-123">-CommonName</span></span>
<span data-ttu-id="90f83-124">Укажите общее имя сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="90f83-124">Specify client certificate common name.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f83-125">-DefaultProfile</span></span>
<span data-ttu-id="90f83-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90f83-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f83-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="90f83-127">-IssuerThumbprint</span></span>
<span data-ttu-id="90f83-128">Укажите отпечаток поставщика сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="90f83-128">Specify client certificate issuer thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90f83-129">-Name</span></span>
<span data-ttu-id="90f83-130">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="90f83-130">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="90f83-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="90f83-132">Укажите отпечаток сертификата клиента с разрешением только для чтения.</span><span class="sxs-lookup"><span data-stu-id="90f83-132">Specify client certificate thumbprint that has read only permission.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90f83-133">-ResourceGroupName</span></span>
<span data-ttu-id="90f83-134">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90f83-134">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-135">-Отпечаток</span><span class="sxs-lookup"><span data-stu-id="90f83-135">-Thumbprint</span></span>
<span data-ttu-id="90f83-136">Укажите отпечаток сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="90f83-136">Specify client certificate thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90f83-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90f83-137">-Confirm</span></span>
<span data-ttu-id="90f83-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90f83-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f83-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f83-139">-WhatIf</span></span>
<span data-ttu-id="90f83-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90f83-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90f83-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90f83-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f83-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f83-142">CommonParameters</span></span>
<span data-ttu-id="90f83-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90f83-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f83-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90f83-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f83-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90f83-145">INPUTS</span></span>

### <span data-ttu-id="90f83-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90f83-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="90f83-147">System. String</span><span class="sxs-lookup"><span data-stu-id="90f83-147">System.String</span></span>

### <span data-ttu-id="90f83-148">System. String []</span><span class="sxs-lookup"><span data-stu-id="90f83-148">System.String[]</span></span>

### <span data-ttu-id="90f83-149">Microsoft. Azure. Commands. ServiceFabric. Models. PSClientCertificateCommonName []</span><span class="sxs-lookup"><span data-stu-id="90f83-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="90f83-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90f83-150">OUTPUTS</span></span>

### <span data-ttu-id="90f83-151">Microsoft. Azure. Commands. ServiceFabric. Models. PSCluster</span><span class="sxs-lookup"><span data-stu-id="90f83-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="90f83-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="90f83-152">NOTES</span></span>

## <span data-ttu-id="90f83-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90f83-153">RELATED LINKS</span></span>

[<span data-ttu-id="90f83-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="90f83-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
